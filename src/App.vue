<script setup lang="ts">
import { sampleVideos } from './assets/sample.js';
import VideoCard from './components/VideoCard.vue';
</script>

<template>
  <div class="p-6">
    <h1 class="text-2xl font-bold mb-6">Sample Videos</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      <VideoCard v-for="video in sampleVideos" :key="video.videoId" :video="video" />
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
