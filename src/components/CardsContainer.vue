<template>
  <div>
    <div class="group">
      <h1 class="group__title">Играй</h1>
      <div class="group__link" @click="navigateToSection">
        <div>В раздел</div>
        <img class="group__link-arrow" src="@/assets/icons/arrow.svg" />
      </div>
    </div>
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
  </div>
</template>

<script>
import Card from "@/components/Card.vue";
import image1 from "@/assets/images/game1.png";
import image2 from "@/assets/images/ball.png";
import image3 from "@/assets/images/game2.png";

export default {
  name: "CardsContainer",
  components: {
    Card,
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
      // Логика для навигации в нужный раздел
      console.log('Navigating to section');
    },
  },
};
</script>

<style lang="scss" scoped>
.cards-container {
  width: 100%;
  display: flex;
  gap: 20px;
  justify-content: space-around;
  padding: 40px 20px;
}

.group {
  display: flex;
  justify-content: space-between;
  align-items: end;
  margin: 20px 0;
  padding: 0 20px;

  &__title {
    font-size: 5rem;
    font-weight: bold;
    margin: 0;
  }

  &__link {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 1.2rem;
    font-weight: bold;
    color: #f06449;
    cursor: pointer;
    text-decoration: none;
    transition: color 0.3s ease;

    &-arrow {
      stroke: #d9534f;
      fill: black;
    }

    &:hover {
      color: #d9534f;
    }
  }
}
</style>
