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
        Текст кнопки
        <arrow class="card__arrow"/>
      </button>
    </div>
  </template>
  
  <script>
  import arrow from './icons/arrow.vue';
  
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
    components: {
      arrow
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
    width: 100%;
  
    &:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
      background-color: #202020;
      color: #ffffff;
    }
  
    &__image-container {
      display: flex;
      align-items: center;
      overflow: hidden;
      border-radius: 0 0 50vh 50vh;
      transition: transform 0.3s ease;
      margin-bottom: 30px;
    }
  
    &__content {
      margin: 20px;
      text-align: left;
      transition: color 0.3s ease, transform 0.3s ease;
    }
  
    &__title {
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 0.5rem;
      transition: color 0.3s ease;
    }
  
    &__button {
      position: absolute;
      display: flex;
      justify-content: space-between;
      align-items: center;
      bottom: 20px;
      left: 50%;
      width: calc(100% - 40px);
      padding: 1rem;
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
  
    &:hover &__image-container {
      transform: translateY(-80px);
    }
  
    &:hover &__content {
      transform: translateY(-80px);
    }
  
    &:hover &__button {
      opacity: 1;
      visibility: visible;
      transform: translateX(-50%) translateY(0);
    }
  
    &__description {
      padding-top: 10px;
      font-size: 1rem;
      margin: 0;
      width: 75%;
      transition: color 0.3s ease;
    }
  
    &--no-radius &__image-container {
      border-radius: 0;
      transform: translateX(80px);
    }
  
    &--no-radius:hover &__image-container {
      transform: translate(80px, -80px);
    }
  }
  </style>
  