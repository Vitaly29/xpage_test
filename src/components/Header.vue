<template>
  <header class="header">
    <div class="header__group">
      <img class="header__logo" src="@/assets/icons/xpage.svg" alt="xpage">
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
      <button class="header__profile-button">
        <img class="header__profile-icon" src="@/assets/icons/menu.svg">
        <div>Меню</div>
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
  justify-content: space-between;
  align-items: center;
  padding: 0px 20px;
  background-color: #fff;
  border-radius: 20px;
  margin-bottom: 8px;
  height: 80px;

  &__group {
    display: flex;
    align-items: center;
    height: auto;
    gap: 64px;
  }

  &__logo {
    height: auto;
  }

  &__nav {
    &-list {
      display: flex;
      align-items: center;
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
      display: flex;
      align-items: center;
      background: none;
      border: none;
      cursor: pointer;
      background-color: #fff;
      padding: 0;
    }

    &-icon {
      display: flex;
      align-items: center;
      // height: auto;
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
