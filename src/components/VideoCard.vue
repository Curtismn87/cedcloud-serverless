<template>
    <div class="border rounded-lg shadow-md p-4 hover:shadow-lg transition">
      <img :src="video.thumbnail.url" :alt="video.title" class="w-full h-auto mb-4 rounded" />
      <h2 class="text-lg font-semibold">{{ video.title }}</h2>
      <p class="text-sm text-gray-600">{{ video.channelTitle }}</p>
      <p class="text-xs text-gray-500">{{ formattedDate }}</p>
    </div>
  </template>
  
  <script setup lang="ts">
  import { computed } from 'vue';
  
  const props = defineProps<{
    video: {
      videoId: string;
      title: string;
      channelTitle: string;
      publishedAt: string;
      thumbnail: {
        url: string;
      };
    };
  }>();
  
  const formattedDate = computed(() => {
    return new Date(props.video.publishedAt).toLocaleDateString();
  });
  </script>