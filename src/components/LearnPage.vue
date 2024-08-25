<template>
  <div class="page">
    <!-- Заголовок страницы -->
    <header class="header">
      <h1 class="header__title">УЧИСЬ</h1>
      <div class="header__link">
        В РАЗДЕЛ
        <arrow class="arrow" />
      </div>
    </header>

    <!-- Основное содержимое страницы -->
    <main class="main-content">
      <div class="main-content__left">
        <!-- Главный баннер -->
        <section class="main-banner">
          <img src="@/assets/images/1.webp" alt="Main Banner" class="main-banner__image" />
          <div class="main-banner__text">
            <h2>МЫ СОБРАЛИ СЕКЦИИ ДЛЯ ДЕТЕЙ ПО ВСЕМУ ГОРОДУ</h2>
            <div class="card__tags">
              <span>12 СЕКЦИЙ ПО ВСЕМУ ГОРОДУ</span>
            </div>
          </div>
        </section>

        <!-- Карточки под баннером -->
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

      <!-- Боковая панель -->
      <aside class="sidebar">
        <!-- Видеоуроки -->
        <div class="sidebar__section">
          <h3>ВИДЕОУРОКИ</h3>
          <div class="sidebar__section__item">
            <img src="@/assets/images/game3.png" alt="Видео урок" class="sidebar__image" />
            <div class="sidebar__info">
              <div>Евгений Воронов: "Бронзовые медали - оценка труда нашей команды"</div>
              <div class="sidebar__info__tags">
                <span>26 октября</span>
              </div>
            </div>
          </div>
        </div>

        <div class="divider"></div>

        <!-- Статьи -->
        <div class="sidebar__section">
          <h3 class="header__link">
            СТАТЬИ
            <arrow />
          </h3>

          <div class="sidebar__section__item">
            <div class="sidebar__info">
              <div>Евгений Воронов: "Бронзовые медали - оценка труда нашей команды"</div>
              <div class="sidebar__info__tags">
                <span>26 октября</span>
              </div>
            </div>
          </div>
        </div>

        <div class="divider"></div>
        
        <!-- Термины -->
        <div class="sidebar__section">
          <h3>ТЕРМИНЫ</h3>
          <div class="sidebar__section__item">
            <div class="sidebar__info__tags">
              <span>Треха</span>
              <span>Трехочковый бросок</span>
              <span>36 терминов</span>
            </div>
          </div>
        </div>
      </aside>
    </main>
  </div>
</template>

<script>
import arrow from './icons/arrow.vue'
export default {
  name: "LearnPage",
  components: {
    arrow
  },
};
</script>

<style lang="scss" scoped>
.page {
  margin-top: 80px;
  background-color: white;
  border-radius: 20px;
  padding: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;

  &__title {
    font-size: 4rem;
  }

  &__link {
    display: flex;
    align-items: center;
    gap: 1rem;
    color: #008000;
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
  flex: 1.5;
  display: flex;
  flex-direction: column;
  position: relative;
}

.main-banner {
  position: relative;
  background-color: #f5f5f5;
  border-radius: 20px;
  overflow: hidden;
  margin-bottom: 20px;
  height: 100%;

  &__text {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    position: absolute;
    padding: 10px;
    top: 0px;
    left: 0px;
    color: white;
    z-index: 1;
    height: 100%;

    h2 {
      font-size: 2.5rem;
      font-weight: bold;
      width: 75%;
    }

    span {
      font-size: 1rem;
      background-color: white;
      color: green;
      padding: 5px 10px;
      border-radius: 5px;
    }
  }

  &__image {
    width: 170%;
    height: 100%;
    overflow: hidden;
    position: relative;
    object-fit: cover;
    object-position: top;
  }
}

.cards-section {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 50px;
  height: 100%;

  .card {
    background-color: #008000;
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
        color: #006600;
        padding: 5px 10px;
        border-radius: 10px;
      }

      span {
        background-color: #006600;
        padding: 5px 10px;
        border-radius: 10px;
      }
    }
  }
}

.sidebar {
  flex: 1;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  gap: 1rem;
  border-left: 2px solid #e0e0e0;
  padding-left: 20px;

  &__section {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    h3 {
      font-size: 1.2rem;
      margin-bottom: 10px;
    }

    &__item {
      display: flex;
      gap: 10px;

      .sidebar__image {
        object-fit: cover;
        border-radius: 10px;
      }

      .sidebar__info {
        height: auto;
        width: 75%;
        display: flex;
        justify-content: space-between;
        flex-direction: column;

        gap: 10px;

        &__tags {
          display: flex;
          flex-wrap: wrap;
          gap: 8px;

          span {
            background-color: #EFEFEF;
            padding: 5px;
            border-radius: 25px;
            font-size: 1rem;
          }
        }
      }
    }

    &__tags {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;

      span {
        background-color: #e0e0e0;
        padding: 5px 10px;
        border-radius: 10px;
        font-size: 0.9rem;
      }
    }
  }
}

.divider {
  height: 5px;
  background-color: #e0e0e0;
  width: 100%;
  align-self: center;
}

.arrow {
  color: green;
}
</style>
