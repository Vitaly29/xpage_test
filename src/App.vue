<template>
  <div id="app">
    <Header />
    <Banner />
    <CardsContainer />
    <LearnPage />
  </div>
</template>

<script setup lang="ts">
import Header from '@/components/Header.vue';
import Banner from '@/components/Banner.vue';
import CardsContainer from '@/components/CardsContainer.vue';
import LearnPage from "@/components/LearnPage.vue";
</script>

<style lang="scss">
@import '@/assets/styles/main.scss';
</style>
