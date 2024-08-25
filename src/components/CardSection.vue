<template>
    <section class="card-section">
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
  </template>
  
  <script>
  export default {
    name: 'CardSection',
  };
  </script>
  
  <style lang="scss" scoped>
  .card-section {
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
  