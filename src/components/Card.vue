<template>
    <div class="card" :class="{ 'card--no-radius': noRadius, 'card--shift-right': shiftRight }">
        <div class="card__image-container">
            <img :src="image" alt="Card Image" class="card__image" />
        </div>
        <div class="card__content">
            <h3 class="card__title">{{ title }}</h3>
            <p class="card__description">{{ description }}</p>
        </div>
        <button class="card__button">
            Кнопка
            <img src="@/assets/icons/arrow.svg">
        </button>
    </div>
</template>


<script>
export default {
    name: "Card",
    props: {
        image: {
            type: String,
            required: true,
        },
        title: {
            type: String,
            required: true,
        },
        description: {
            type: String,
            required: true,
        },
        noRadius: {
            type: Boolean,
            default: false,
        },
        shiftRight: {
            type: Boolean,
            default: false,
        },
    },
};
</script>

<style lang="scss" scoped>
.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #ffffff;
    border-radius: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
    position: relative;
    overflow: hidden;

    &:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        background-color: #202020; // Серый фон при наведении
        color: #ffffff;
    }

    &__image-container {
        display: flex;
        align-items: center;
        width: auto;
        height: auto;
        overflow: hidden;
        position: relative;
        border-radius: 0 0 50vh 50vh;
        object-fit: cover;
        object-position: bottom;
        transition: transform 0.3s ease;
    }

    &__image {
        width: auto;
        object-fit: cover;
        object-position: bottom;
        transition: transform 0.3s ease;
    }

    &__content {
        margin: 20px;
        text-align: left;
        transition: color 0.3s ease, transform 0.3s ease;
    }

    &__title {
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 0.5rem;
        width: 70%;
        transition: color 0.3s ease;
    }

    &__button {
        position: absolute;
        display: flex;
        justify-content: space-between;
        bottom: 20px;
        left: 50%;
        width: calc(100% - 40px);
        padding: 1rem 1rem;
        border: none;
        border-radius: 20px;
        cursor: pointer;
        font-size: 1rem;
        font-weight: bold;
        text-align: left;
        color: white;
        background-color: #F36722;
        transform: translateX(-50%) translateY(100%);
        opacity: 0;
        visibility: hidden;
        transition: opacity 0.3s ease, visibility 0.3s ease, transform 0.3s ease;
    }

    &:hover .card__image-container {
        transform: translateY(-80px);
    }

    &:hover .card__content {
        transform: translateY(-80px);
    }

    &:hover .card__button {
        opacity: 1;
        visibility: visible;
        transform: translateX(-50%) translateY(0);
    }

    &__description {
        font-size: 1rem;
        margin: 0;
        height: auto;
        transition: color 0.3s ease;
    }

    &--no-radius {
        .card__image-container {
            border-radius: 0;
            transform: translateX(80px);
        }

        &:hover {
            .card__image-container {
                transform: translate(80px, -80px);
            }
        }
    }


}
</style>
