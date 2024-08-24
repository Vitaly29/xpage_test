<!-- LearnPage.vue -->
<template>
  <div class="page">
    <!-- Заголовок страницы -->
    <header class="header">
      <h1 class="header__title">УЧИСЬ</h1>
      <div class="header__link">В РАЗДЕЛ ➔</div>
    </header>

    <!-- Основное содержимое страницы -->
    <main class="main-content">
      <div class="main-content__left">
        <!-- Главный баннер -->
        <section class="main-banner">
          <img src="@/assets/images/1.webp" alt="Main Banner" class="main-banner__image"/>
          <div class="main-banner__text">
            <h2>Мы собрали секции для детей по всему городу</h2>
            <span>12 СЕКЦИЙ ПО ВСЕМУ ГОРОДУ</span>
          </div>
        </section>

        <!-- Карточки под баннером -->
        <section class="cards-section">
          <div class="card">
            <h3 class="card__title">Подбери тренера под свой уровень</h3>
            <div class="card__tags">
              <span>Детская тренировка</span>
              <span>Для начинающих</span>
              <span>Стритбол</span>
              <span>Выезд тренера на дом</span>
              <span>12 фильтров</span>
            </div>
          </div>
        </section>
      </div>

      <!-- Боковая панель -->
      <aside class="sidebar">
        <!-- Видеоуроки -->
        <div class="sidebar__section">
          <h3>ВИДЕОУРОКИ</h3>
          <div class="sidebar__item">
            <img src="@/assets/images/game3.png" alt="Видео урок" class="sidebar__thumbnail"/>
            <div class="sidebar__info">
              <p>Евгений Воронов: "Бронзовые медали - оценка труда нашей команды"</p>
              <span>26 октября</span>
            </div>
          </div>
        </div>

        <!-- Статьи -->
        <div class="sidebar__section">
          <h3>СТАТЬИ ➔</h3>
          <div class="sidebar__item">
            <!-- <img src="@/assets/images/article-thumbnail.jpg" alt="Статья" class="sidebar__thumbnail"/> -->
            <div class="sidebar__info">
              <p>Евгений Воронов: "Бронзовые медали - оценка труда нашей команды"</p>
              <span>26 октября</span>
            </div>
          </div>
        </div>

        <!-- Термины -->
        <div class="sidebar__section">
          <h3>ТЕРМИНЫ</h3>
          <div class="sidebar__tags">
            <span>Треха</span>
            <span>Трехочковый бросок</span>
            <span>36 терминов</span>
          </div>
        </div>
      </aside>
    </main>
  </div>
</template>

<script>
export default {
  name: "LearnPage"
};
</script>

<style lang="scss" scoped>
.page {
  padding: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;

  &__title {
    font-size: 5rem;
    font-weight: bold;
    margin: 0;
  }

  &__link {
    color: #008000; /* Зеленый цвет текста для соответствия картинке */
    cursor: pointer;
    font-size: 1.2rem;
    font-weight: bold; /* Жирный шрифт для выделения */
    text-decoration: none; /* Убираем подчеркивание */
  }
}

.main-content {
  display: flex;
  gap: 20px; /* Отступ между основной колонкой и боковой панелью */
}

.main-content__left {
  flex: 3; /* Основная часть занимает больше места */
  display: flex;
  flex-direction: column;
}

.main-banner {
  position: relative;
  background-color: #f5f5f5;
  border-radius: 20px;
  overflow: hidden;
  margin-bottom: 20px;
  width: 100%; /* Полная ширина */
  height: 300px; /* Фиксированная высота баннера */

  &__text {
    position: absolute;
    top: 50%; /* Центрирование по вертикали */
    left: 20px;
    transform: translateY(-50%); /* Центрирование текста по вертикали */
    color: white;
    z-index: 1;
    width: 50%; /* Ограничиваем ширину текста для лучшего размещения */

    h2 {
      font-size: 2.5rem; /* Немного увеличиваем размер шрифта */
      font-weight: bold;
      margin: 0; /* Убираем отступы */
      line-height: 1.2; /* Регулируем межстрочный интервал для лучшей читабельности */
    }

    span {
      font-size: 1rem;
      display: block;
      margin-top: 10px;
      background-color: #008000; /* Зеленый фон для соответствия стилю */
      padding: 5px 10px;
      border-radius: 5px; /* Скругленные углы */
    }
  }

  &__image {
    width: 100%;
    height: 100%;
    object-fit: cover; /* Картинка обрезается, чтобы заполнить контейнер */
    object-position: center; /* Картинка центрируется */
  }
}

.cards-section {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin-bottom: 20px;

  .card {
    background-color: #008000; /* Зеленый фон для соответствия стилю */
    color: white;
    padding: 20px;
    border-radius: 20px;
    flex: 1;

    &__title {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }

    &__tags {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;

      span {
        background-color: #006600;
        padding: 5px 10px;
        border-radius: 10px;
      }
    }
  }
}

.sidebar {
  flex: 1; /* Боковая панель занимает меньше места */
  display: flex;
  flex-direction: column;
  gap: 20px;

  &__section {
    background-color: #ffffff;
    padding: 15px;
    border-radius: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);

    h3 {
      font-size: 1.2rem;
      margin-bottom: 10px;
    }

    &__item {
      display: flex;
      gap: 10px;
      margin-bottom: 10px;

      .sidebar__thumbnail {
        width: 100px; /* Увеличиваем размер изображения */
        height: 70px;
        object-fit: cover;
        border-radius: 10px;
      }

      .sidebar__info {
        p {
          font-size: 0.9rem;
          margin-bottom: 5px;
        }

        span {
          font-size: 0.8rem;
          color: gray;
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

</style>
