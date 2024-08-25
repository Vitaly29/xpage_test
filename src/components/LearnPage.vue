<template>
  <div class="page">
    <header class="header">
      <h1 class="header__title">УЧИСЬ</h1>
      <div class="header__link">
        В РАЗДЕЛ
        <arrow class="arrow" />
      </div>
    </header>

    <main class="main-content">
      <div class="main-content__left">
        <section class="main-banner">
          <img src="@/assets/images/1.webp" alt="Main Banner" class="main-banner__image" />
          <div class="main-banner__text">
            <h2>МЫ СОБРАЛИ СЕКЦИИ ДЛЯ ДЕТЕЙ ПО ВСЕМУ ГОРОДУ</h2>
            <div class="main-banner__text__tags">
              <span>12 СЕКЦИЙ ПО ВСЕМУ ГОРОДУ</span>
            </div>
          </div>
        </section>

        <section class="cards-section">
          <div class="card">
            <h3 class="card__title">ПОДБЕРИ ТРЕНЕРА ПОД СВОЙ УРОВЕНЬ</h3>
            <div class="card__tags">
              <span>Детская тренировка</span>
              <span>Для начинающих</span>
              <span>Стритбол</span>
              <span>Выезд тренера на дом</span>
              <span class="filter">12 фильтров</span>
            </div>
          </div>
        </section>
      </div>

      <Sidebar />
    </main>
  </div>
</template>

<script>
import arrow from './icons/arrow.vue';
import Sidebar from '@/components/Sidebar.vue';

export default {
  name: "LearnPage",
  components: {
    arrow,
    Sidebar
  },
};
</script>

<style lang="scss" scoped>
.page {
  margin-top: 100px;
  background-color: white;
  border-radius: 20px;
  padding: 30px;
}

.header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 50px;
  margin-top: 10px;

  &__title {
    font-size: 4rem;
  }

  &__link {
    display: flex;
    align-items: end;
    gap: 1rem;
    color: #2E8D43;
    cursor: pointer;
    font-size: 1.2rem;
    text-decoration: none;
  }
}

.main-content {
  display: flex;
  gap: 20px;
}

.main-content__left {
  flex: 2;
  display: flex;
  flex-direction: column;
  position: relative;
}

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

.cards-section {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 50px;
  height: 100%;

  .card {
    background-color: #2E8D43;
    color: white;
    padding: 20px;
    border-radius: 20px;
    display: flex;
    gap: 50px;
    justify-content: space-between;
    flex-direction: column;

    &__title {
      font-size: 2.5rem;
      margin-bottom: 10px;
      width: 75%;
    }

    &__tags {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      width: 75%;

      .filter {
        background-color: white;
        color: #2E8D43;
        padding: 10px 15px;
        border-radius: 40px;
      }

      span {
        background-color: rgba(255, 255, 255, 0.2);
        padding: 10px 15px;
        border-radius: 40px;
      }
    }
  }
}
</style>
