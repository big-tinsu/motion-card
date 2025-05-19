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
  location: 'Eiffel Tower',
  sub_location: 'Paris, France',
  image: '/src/assets/images/eiffel-tower.png',
  mode: 'Dark',
}
</script>

<style lang="scss" scoped>
#app {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
