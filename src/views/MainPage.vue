<template>
  <div>
    <PokemonSearch @pokemon-fetched="handleData"/>
    <PokemonSprite :pokemonFetched/>
    <ShowStats :pokemonFetched />
  </div>
</template>

<script setup lang="ts">
import PokemonSearch from '@/components/PokemonSearch.vue'
import PokemonSprite from '@/components/PokemonSprite.vue';
import ShowStats from '@/components/ShowStats.vue';

import { ref } from 'vue';
const pokemonFetched = ref('')

const handleData = (data: string) => {
  pokemonFetched.value = data
  console.log(pokemonFetched.value)
}
</script>

<style scoped>
</style>
