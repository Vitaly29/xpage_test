<template>
  <div class="page">
    <header class="page__header">
      <h1 class="page__title">ИГРАЙ</h1>
      <div class="page__link" @click="navigateToSection">
        В РАЗДЕЛ
        <arrow class="page__arrow" />
      </div>
    </header>
    <main class="page__content">
      <div class="cards-container">
        <Card 
          v-for="(card, index) in cards" 
          :key="index" 
          :image="card.image" 
          :title="card.title"
          :description="card.description" 
          :noRadius="index === 1" 
          :shiftRight="index === 1" 
        />
      </div>
    </main>
  </div>
</template>

<script>
import Card from "@/components/Card.vue";
import image1 from "@/assets/images/game1.png";
import image2 from "@/assets/images/ball.png";
import image3 from "@/assets/images/game2.png";
import arrow from '@/components/icons/arrow.vue';

export default {
  name: "CardsContainer",
  components: {
    Card,
    arrow
  },
  data() {
    return {
      cards: [
        {
          image: image1,
          title: "Найди себе команду",
          description:
            "Игры на районе - это возможность найти с кем поиграть в баскетбол в выходные, или создать свою игру и пригласить других игроков присоединиться.",
        },
        {
          image: image2,
          title: "Создавай команды",
          description:
            "Игры на районе - это возможность найти с кем поиграть в баскетбол в выходные, или создать свою игру и пригласить других игроков присоединиться.",
        },
        {
          image: image3,
          title: "Участвуй в турнирах",
          description:
            "Участвуйте в турнирах вместе с вашей командой. Будьте активными, побеждайте и получайте призы и признание от наших спонсоров.",
        },
      ],
    };
  },
  methods: {
    navigateToSection() {
      console.log('Navigating to section');
    },
  },
};
</script>

<style lang="scss" scoped>
.page {
  margin-top: 100px;

  &__header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 60px;
  }

  &__title {
    font-size: 4rem;
  }

  &__link {
    display: flex;
    align-items: end;
    gap: 1rem;
    color: #f06449;
    cursor: pointer;
    font-size: 1.2rem;
    text-decoration: none;
  }

  &__arrow {
    color: inherit;
  }

  &__content {
    display: flex;
    justify-content: space-around;
    gap: 10px;
  }
}

.cards-container {
  width: 100%;
  display: flex;
  gap: 10px;
  justify-content: space-around;
}
</style>
