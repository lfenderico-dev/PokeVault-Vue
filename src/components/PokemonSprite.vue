<template>
  <div v-if="pokemonFetched " class="bg-fuchsia-800/80 hover:bg-sky-700/80 rounded-3xl absolute bottom-40 left-90 m-15 p-5 ">
    <img class="h-110 w-110"   :src="pokemonFetched.sprites.front_default" alt="pokemon sprite">
  </div>
</template>

<script setup lang="ts">

defineProps(['pokemonFetched'])
</script>

<style scoped>

</style>
