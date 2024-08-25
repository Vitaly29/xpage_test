<template>
  <header class="header">
    <div class="header__group">
      <img class="header__logo" src="@/assets/icons/xpage.svg" alt="xpage" />
      <nav class="header__nav">
        <ul class="header__nav-list">
          <li class="header__nav-item"><a href="#" class="header__nav-link">ИГРАТЬ</a></li>
          <li class="header__nav-item"><a href="#" class="header__nav-link">СМОТРЕТЬ</a></li>
          <li class="header__nav-item"><a href="#" class="header__nav-link">УЧИТЬСЯ</a></li>
          <li class="header__nav-item"><a href="#" class="header__nav-link">МЕРОПРИЯТИЯ</a></li>
        </ul>
      </nav>
    </div>
    <div class="header__profile">
      <button class="header__profile-button">
        <img class="header__profile-icon" src="@/assets/icons/menu.svg" alt="Меню" />
        МЕНЮ
      </button>
      <div class="header__profile-user">
        <span class="header__profile-user-name">
          ГЕНАДИЙ П.
          <img src="@/assets/images/user.png" alt="Пользователь" class="header__profile-user-image" />
        </span>
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
  padding: 0 20px;
  background-color: #fff;
  border-radius: 20px;
  margin-bottom: 8px;
  height: 80px;
  font-size: 0.8rem;

  &__group {
    display: flex;
    align-items: center;
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

      &:hover {
        color: $primary-color;
      }
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
      padding: 0;
      gap: 8px;
    }

    &-icon {
      display: flex;
      align-items: center;
    }

    &-user {
      display: flex;
      align-items: center;
      gap: 0.5rem;

      &-name {
        display: flex;
        align-items: center;
        gap: 10px;
        background-color: #efefef;
        padding: 3px 3px 3px 15px;
        border-radius: 25px;
      }

      &-image {
        border-radius: 100%;
      }
    }
  }
}
</style>
