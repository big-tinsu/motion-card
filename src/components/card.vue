<template>
  <div :class="props.card.mode === 'Dark' ? 'bg-black' : 'bg-white'" class="rounded-[2rem] p-1 w-[300px] h-[300px] md:w-[400px] md:h-[300px]">
    <img
      :src="props.card.image"
      alt="card"
      class="w-full h-[200px] rounded-t-[2rem] rounded-b-[1rem]"
    />
    <div class="flex justify-between items-center h-[100px] px-2.5">
      <div class="text-black text-left">
        <p :class="props.card.mode === 'Dark' && 'text-white' " class=" text-lg md:text-xl font-bold">{{ props.card.location }},</p>
        <p class="text-sm text-gray-500">{{ props.card.sub_location }}</p>
      </div>
      <div>
        <button class="bg-gray-100 rounded-full p-2 flex items-center gap-2">
          <img
            src="../assets/logos/locate.png"
            alt="directions"
            class="w-6 h-6"
          />
          Directions
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
  mode: string;
}

const props = defineProps<{
  card: Card
}>()
</script>
