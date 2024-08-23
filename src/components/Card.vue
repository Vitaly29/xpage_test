<template>
    <div class="card">
        <div class="card__image-container">
            <img :src="image" alt="Card Image" class="card__image" />
        </div>
        <div class="card__content">
            <h3 class="card__title">{{ title }}</h3>
            <p class="card__description">{{ description }}</p>
        </div>
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
    overflow: hidden;
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;

    &:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }

    &__image-container {
        width: 100%;
        overflow: hidden;
        position: relative;
        border-bottom-left-radius: 50% 20%;
        border-bottom-right-radius: 50% 20%;
    }

    &__image {
        width: 100%;
        height: 100%;
        object-fit: cover;
        // border-bottom-left-radius: 100%;
        // border-bottom-right-radius: 100%;
    }

    &__content {
        padding: 20px;
        background-color: #ffffff;
        text-align: left;
    }

    &__title {
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 0.5rem;
    }

    &__description {
        font-size: 1rem;
        margin: 0;
    }
}
</style>