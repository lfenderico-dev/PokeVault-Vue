<template>
  <div>
    <img v-if="pokemonFetched" :src="pokemonFetched.sprites.front_default" alt="pokemon sprite">
  </div>
</template>

<script setup lang="ts">

defineProps(['pokemonFetched'])
</script>

<style scoped>

</style>
