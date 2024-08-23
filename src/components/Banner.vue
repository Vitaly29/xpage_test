<template>
    <div class="banner">
        <img :src="currentImage" alt="Basketball game" class="banner__image" />
        <div class="banner__content">
            <h1 class="banner__content__title">{{ currentTitle }}</h1>
            <div class="banner__content__buttons">
                <button
                    class="banner__button"
                    :class="{ active: activeButton === 'play' }"
                    @mouseover="setContent('play')"
                >
                    Играй
                </button>
                <button
                    class="banner__button"
                    :class="{ active: activeButton === 'learn' }"
                    @mouseover="setContent('learn')"
                >
                    Учись
                </button>
                <button
                    class="banner__button"
                    :class="{ active: activeButton === 'watch' }"
                    @mouseover="setContent('watch')"
                >
                    Смотри
                </button>
            </div>
        </div>
    </div>
</template>
<script>
import image1 from '@/assets/images/1.webp';
import image2 from '@/assets/images/2.webp';
import image3 from '@/assets/images/3.webp';

export default {
    name: 'Banner',
    data() {
        return {
            image1,
            image2,
            image3,
            title1: 'Найди с кем поиграть в баскет',
            title2: 'Учись и развивайся!',
            title3: 'Смотри и вдохновляйся!',
            currentImage: image1,
            currentTitle: 'Найди с кем поиграть в баскет',
            activeButton: 'play', // Начальное активное состояние
        };
    },
    methods: {
        setContent(type) {
            this.activeButton = type; // Устанавливаем текущий активный раздел
            switch (type) {
                case 'play':
                    this.currentImage = this.image1;
                    this.currentTitle = this.title1;
                    break;
                case 'learn':
                    this.currentImage = this.image2;
                    this.currentTitle = this.title2;
                    break;
                case 'watch':
                    this.currentImage = this.image3;
                    this.currentTitle = this.title3;
                    break;
            }
        }
    },
};
</script>
<style lang="scss" scoped>
@import '@/assets/styles/_variables';

.banner {
    position: relative;
    text-align: center;
    color: white;

    &__image {
        width: 100%;
        height: auto;
        border-radius: 15px;
        transition: opacity 0.5s ease;
    }

    &__content {
        position: absolute;
        bottom: 20px;
        left: 20px;
        right: 20px;
        text-align: left;

        &__title {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        &__buttons {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 0.3rem;
        }
    }

    &__button {
        width: 100%;
        padding: 0.75rem 1.5rem;
        border: none;
        border-radius: 15px;
        cursor: pointer;
        font-size: 1rem;
        text-align: left;
        background-color: #fff;
        transition: background-color 0.5s ease, color 0.5s ease;

        &:hover {
            color: white;
            background-color: orangered;
        }

        &.active {
            background-color: orangered; /* Цвет активного раздела */
            color: white;
        }
    }
}
</style>
