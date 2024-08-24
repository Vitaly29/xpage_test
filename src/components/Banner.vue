<template>
  <div class="banner">
    <img :src="currentImage" alt="Basketball game" class="banner__image" />
    <div class="banner__content">
      <h1 class="banner__content__title">{{ currentTitle }}</h1>
      <div class="banner__content__buttons">
        <button class="banner__button" :class="{ active: activeButton === 'play' }" @mouseover="setContent('play')">
          Играй
          <arrow class="arrow"/>
        </button>
        <button class="banner__button" :class="{ active: activeButton === 'learn' }" @mouseover="setContent('learn')">
          Учись
          <arrow class="arrow"/>
        </button>
        <button class="banner__button" :class="{ active: activeButton === 'watch' }" @mouseover="setContent('watch')">
          Смотри
          <arrow class="arrow"/>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import image1 from '@/assets/images/1.webp';
import image2 from '@/assets/images/2.webp';
import image3 from '@/assets/images/3.webp';
import arrow from './icons/arrow.vue';
// Данные
const image1Title = 'Найди с кем поиграть в баскет';
const image2Title = 'Учись и развивайся!';
const image3Title = 'Смотри и вдохновляйся!';

// Реактивные состояния
const currentImage = ref(image1);
const currentTitle = ref(image1Title);
const activeButton = ref('play');

// Методы
const setContent = (type: string) => {
  activeButton.value = type;
  switch (type) {
    case 'play':
      currentImage.value = image1;
      currentTitle.value = image1Title;
      break;
    case 'learn':
      currentImage.value = image2;
      currentTitle.value = image2Title;
      break;
    case 'watch':
      currentImage.value = image3;
      currentTitle.value = image3Title;
      break;
  }
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_variables';

.banner {
  // position: relative;
  // text-align: center;
  color: white;


  &__image {
    width: 100%;
    height: auto;
    border-radius: 20px;
    transition: opacity 0.5s ease;
  }

  &__content {
    position: absolute;
    bottom: 20px;
    left: 20px;
    right: 20px;
    text-align: left;

    &__title {
      width: 80%;
      font-size: 6rem;
      margin-bottom: 1rem;
    }

    &__buttons {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 0.5rem;
    }

    .arrow {
      color: #fff;
    }
  }

  &__button {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    padding: 1rem 1rem;
    border: none;
    border-radius: 15px;
    cursor: pointer;
    font-size: 1rem;
    font-weight: bold;
    text-align: left;
    background-color: #fff;
    transition: background-color 0.5s ease, color 0.5s ease;

    &:hover {
      color: white;
      background-color: #F36722;
    }

    &.active {
      background-color: #F36722;
      color: white;
    }

    .group__link-arrow {
      color: green;
      /* Или любой другой цвет */
    }
  }
}
</style>