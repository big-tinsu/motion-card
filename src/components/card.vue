<template>
  <div class="card">
    <img :src="props.card.image" alt="card" />
    <div>
      <div>
        <p>{{ props.card.location }}</p>
        <p>{{ props.card.sub_location }}</p>
      </div>
      <div>
        <button>
          <img src="@/assets/images/icons/play.svg" alt="play" />
        </button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Card {
  id: number
  location: string
  sub_location: string
  image: string
  mode: string
}

const props = defineProps<{
  card: Card
}>()
</script>
