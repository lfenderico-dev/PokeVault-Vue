<template>
  <header class="bg-fuchsia-800/30 h-15 flex flex-row items-center gap-40 justify-center">
    <nav class="w-fit flex gap-10 justify-center">
      <router-link to="/"><i class="fa-solid fa-house-user text-4xl"></i></router-link>
      <h1 class="text-4xl">PokeVault!</h1>
    </nav>

    <nav class="w-fit flex gap-10 justify-center">
      <a class="text-4xl" href="https://pokeapi.co/">API</a>
      <i
        @mouseover="$emit('showInfoBox')"
        @mouseout="$emit(`hideInfoBox`)"
        class="fa-solid fa-circle-info text-4xl"
      ></i>
    </nav>
  </header>
</template>

<script setup lang="ts"></script>

<style scoped></style>
