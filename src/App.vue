<template>
  <div id="app">
    <Card :card="card" />
    <Card :card="card2" />
  </div>
</template>

<script setup lang="ts">
import Card from './components/card.vue'

const card = {
  id: 1,
  location: 'Colosseum',
  sub_location: 'Rome, Italy',
  image: '/src/assets/images/colosseum.png',
  mode: 'Light',
}

const card2 = {
  id: 2,
  location: 'Chichen Itza',
  sub_location: 'Mexico',
  image: '/src/assets/images/chichen_itza.png',
  mode: 'Dark',
}
</script>

<style lang="scss" scoped>
#app {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  @media (max-width: 768px) {
    flex-direction: column;
  }
}
</style>
