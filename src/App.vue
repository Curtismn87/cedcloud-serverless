<script setup lang="ts">
import { sampleVideos } from './assets/sample.ts'
import VideoGrid from './components/VideoGrid.vue'
</script>

<template>
  <main class="min-h-screen bg-slate-900 text-slate-100">
    <VideoGrid :videos="sampleVideos" />
  </main>
</template>

<style scoped>
/* Removed unused .logo styles to keep the file clean */
</style>
