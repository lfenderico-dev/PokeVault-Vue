<template>
  <div v-if="pokemonFetched">
    <ul>
      <li><strong>Name:</strong> {{ pokemonFetched.name }}</li>
      <li><strong>Types:</strong> {{ pokemonType }}</li>
      <li><strong>Id:</strong> {{ pokemonFetched.id }}</li>
      <li><strong>Height:</strong> {{ pokemonFetched.height }}m</li>
      <li><strong>Weight:</strong> {{ pokemonFetched.weight }}kg</li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
const props = defineProps(['pokemonFetched'])

const pokemonType = computed(() => {
   const pokemonTypes = props.pokemonFetched.types.map(x => x.type.name)
   return pokemonTypes.join(', ')
})
</script>

<style scoped>

</style>
