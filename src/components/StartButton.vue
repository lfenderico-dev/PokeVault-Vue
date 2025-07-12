<template>
  <div class="flex justify-center items-center h-screen">
    <button
      class="bg-sky-800/70 px-5 h-50 w-210 rounded-2xl text-4xl hover:bg-sky-800/90 hover:animate-bounce"
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
