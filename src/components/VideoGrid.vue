<template>
    <div class="py-8 px-4 max-w-screen-xl mx-auto">
      <h1 class="text-3xl font-bold text-slate-100 mb-6 text-center">Featured MIT Lectures</h1>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <VideoCard
          v-for="video in videos"
          :key="video.videoId"
          :video="video"
        />
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import VideoCard from './VideoCard.vue'
  import { sampleVideos } from '../assets/sample.js'
  
  const videos = sampleVideos
  </script>
  