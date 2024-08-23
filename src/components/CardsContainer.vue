<template>
  <div>
    <div class="group">
      <h1 class="group__title">Играй</h1>
      <div class="group__link">В раздел -></div>
    </div>
    <div class="cards-container">
      <Card
        v-for="(card, index) in cards"
        :key="index"
        :image="card.image"
        :title="card.title"
        :description="card.description"
      />
    </div>
  </div>
</template>

<script>
import Card from "@/components/Card.vue";
import image1 from "@/assets/images/1.webp";

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
          image: image1,
          title: "Создавай команды",
          description:
            "Игры на районе - это возможность найти с кем поиграть в баскетбол в выходные, или создать свою игру и пригласить других игроков присоединиться.",
        },
        {
          image: image1,
          title: "Участвуй в турнирах",
          description:
            "Участвуйте в турнирах вместе с вашей командой. Будьте активными, побеждайте и получайте призы и признание от наших спонсоров.",
        },
      ],
    };
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
  padding-left: 20px;
  padding-right: 20px;

  &__title {
    font-size: 5rem; 
    font-weight: bold; 
    margin: 0; 
  }

  &__link {
    font-size: 1.2rem; 
    font-weight: bold; 
    color: #f06449;
    cursor: pointer; 
    text-decoration: none; 
    transition: color 0.3s ease; 

    &:hover {
      color: #d9534f; 
    }
  }
}
</style>
