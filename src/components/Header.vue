<template>
  <header class="header">
    <div class="header__group">
      <div class="header__logo">
        XPAGE
      </div>
      <nav class="header__nav">
        <ul class="header__nav-list">
          <li class="header__nav-item"><a href="#" class="header__nav-link">Играть</a></li>
          <li class="header__nav-item"><a href="#" class="header__nav-link">Смотреть</a></li>
          <li class="header__nav-item"><a href="#" class="header__nav-link">Учиться</a></li>
          <li class="header__nav-item"><a href="#" class="header__nav-link">Мероприятия</a></li>
        </ul>
      </nav>
    </div>
    <div class="header__profile">
      <button class="header__menu-button">
        Меню
      </button>
      <div class="header__profile-user">
        <span class="header__profile-user-name">Геннадий П.</span>
      </div>
    </div>
  </header>
</template>
  
  <script>
  export default {
    name: 'Header',
  };
  </script>
  
  <style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.header {
  display: flex;
  justify-content: space-between; /* Разместить группы элементов по краям */
  align-items: center;
  padding: 1.2rem;
  background-color: #fff;
  border-radius: 15px;
  margin-bottom: 8px;

  &__group {
    display: flex; /* Новый контейнер для логотипа и навигации */
    align-items: center; /* Выравниваем по центру по вертикали */
    gap: 2.5rem; /* Разделяем логотип и навигацию */
  }

  &__logo {
    font-weight: bold;
  }

  &__nav {
    &-list {
      display: flex;
      gap: 1.5rem;
      list-style: none;
      padding: 0;
      margin: 0;
    }

    &-link {
      text-decoration: none;
      color: #000;
      font-weight: bold;
    }
  }

  &__profile {
    display: flex;
    align-items: center;
    gap: 1rem;

    &-button {
      background: none;
      border: none;
      cursor: pointer;
    }

    &-icon {
      width: 30px;
      height: auto;
    }

    &-user {
      display: flex;
      align-items: center;
      gap: 0.5rem;

      &-name {
        font-weight: bold;
      }
    }
  }
}
</style>
