<template>
  <div class="absolute top-80 m-20 ">
    <img class="h-120 w-120"  v-if="pokemonFetched" :src="pokemonFetched.sprites.front_default" alt="pokemon sprite">
  </div>
</template>

<script setup lang="ts">

defineProps(['pokemonFetched'])
</script>

<style scoped>

</style>
