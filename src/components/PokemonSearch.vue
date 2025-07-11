<template>
  <div class="top-20 left-135 absolute bg-fuchsia-800/30 px-15 py-5 rounded-2xl">
    <label class="text-4xl flex justify-center" for="search">Enter your pokemon:</label><br />
    <div class="flex flex-row gap-5">
      <input
        class="flex justify-center w-130 h-15 bg-sky-700/80 rounded-4xl p-10 text-xl"
        type="text"
        name="search"
        id="search"
        placeholder="What pokemon are you looking for?"
        v-model="pokemonName"
      />
      <button
        class="bg-sky-800/90 rounded-4xl w-40 text-xl hover:bg-sky-600 transition-all duration-300 [transition-timing-function:cubic-bezier(0.175,0.885,0.32,1.275)] active:-translate-y-1 active:scale-x-90 active:scale-y-110"
        @click="fetchData"
      >
        Submit
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const pokemonName = ref('')
const emit = defineEmits(['pokemonFetched'])

async function fetchData(e: { preventDefault: () => void }) {
  e.preventDefault()

  try {
    const result = await fetch(`https://pokeapi.co/api/v2/pokemon/${pokemonName.value}`)

    const data = await result.json()
    console.log(data)

    emit('pokemonFetched', data)

    pokemonName.value = ''
  } catch {
    alert('Error! Maybe that is not a pokemon?')
  }
}
</script>

<style scoped></style>
