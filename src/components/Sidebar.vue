<template>
    <aside class="sidebar">
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
  
      <div class="sidebar__section">
        <h3>ТЕРМИНЫ</h3>
        <div class="sidebar__section__item">
          <div class="sidebar__info__tags">
            <span>Треха</span>
            <span>Трехочковый бросок</span>
            <span class="term">36 терминов</span>
          </div>
        </div>
      </div>
    </aside>
  </template>
  
  <script>
  import arrow from './icons/arrow.vue';
  
  export default {
    name: "Sidebar",
    components: {
      arrow
    },
    props: {
      videoImage: {
        type: String,
        required: true
      }
    }
  };
  </script>
  
  <style lang="scss" scoped>
  .sidebar {
    flex: 1;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    gap: 1rem;
    border-left: 1px solid #C4C4C4;
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
              padding: 10px 15px;
              border-radius: 40px;
              font-size: 12px;
            }
  
            .term {
              background-color: black;
              color: white;
              padding: 10px 15px;
              border-radius: 40px;
            }
          }
        }
      }
  
      &__tags {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
  
        span {
          background-color: #EFEFEF;
          padding: 5px 10px;
          border-radius: 10px;
          font-size: 0.9rem;
        }
      }
    }
  }
  
  .divider {
    height: 1px;
    background-color: #C4C4C4;
    width: 100%;
    align-self: center;
  }
  
  .arrow {
    color: #2E8D43;
  }
  </style>
  