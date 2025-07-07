<template>
  <div>
    <NavBar @showInfoBox="showInfoBox = true" @hideInfoBox="showInfoBox = false" />
    <InfoBox v-if="showInfoBox" />
    <RouterView />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const showInfoBox = ref(false)

import NavBar from './components/NavBar.vue'
import InfoBox from './components/InfoBox.vue'
</script>

<style scoped></style>
