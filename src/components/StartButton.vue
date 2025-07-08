<template>
  <div class="flex justify-center items-center h-screen">
    <button
      class="bg-fuchsia-800/50 h-35 w-140 rounded-2xl text-3xl hover:bg-fuchsia-800/90 hover:animate-bounce"
      @click="goToMain"
    >
      Click here to start your adventure!
    </button>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from 'vue-router'
const router = useRouter()
const goToMain = () => {
  router.push('/main')
}
</script>

<style scoped></style>
