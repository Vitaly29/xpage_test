<template>
    <section class="main-banner">
      <img src="@/assets/images/1.webp" alt="Main Banner" class="main-banner__image" />
      <div class="main-banner__text">
        <h2>МЫ СОБРАЛИ СЕКЦИИ ДЛЯ ДЕТЕЙ ПО ВСЕМУ ГОРОДУ</h2>
        <div class="main-banner__tags">
          <span>12 СЕКЦИЙ ПО ВСЕМУ ГОРОДУ</span>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'MainBanner',
  };
  </script>
  
  <style lang="scss" scoped>
  .main-banner {
    position: relative;
    background-color: white;
    border-radius: 20px;
    overflow: hidden;
    margin-bottom: 20px;
    height: 100%;
  
    &__text {
      display: flex;
      justify-content: space-between;
      flex-direction: column;
      position: absolute;
      padding: 20px;
      top: 0px;
      left: 0px;
      color: white;
      z-index: 1;
      height: 100%;
  
      div {
        margin-bottom: 10px;
      }
  
      span {
        font-size: 1rem;
        background-color: white;
        color: #2E8D43;
        padding: 10px 15px;
        border-radius: 40px;
      }
  
      h2 {
        font-size: 3rem;
        font-weight: bold;
        width: 70%;
      }
    }
  
    &__image {
      width: 120%;
      height: 120%;
      overflow: hidden;
      position: relative;
      object-fit: cover;
      object-position: left top;
    }
  }
  </style>
  