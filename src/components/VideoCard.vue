<template>
  <div
    class="bg-slate-800 rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow duration-300"
  >
    <img
      :src="video.thumbnail.url"
      :alt="video.title"
      class="w-full h-48 object-cover"
    />
    <div class="p-4">
      <h2 class="text-lg font-semibold text-slate-100 mb-1 truncate">
        {{ video.title }}
      </h2>
      <p class="text-sm text-slate-300 mb-1">{{ video.channelTitle }}</p>
      <p class="text-xs text-slate-400">{{ formattedDate }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  video: {
    videoId: string
    title: string
    channelTitle: string
    publishedAt: string
    thumbnail: {
      url: string
    }
  }
}>()

const formattedDate = computed(() =>
  new Date(props.video.publishedAt).toLocaleDateString(undefined, {
    year: 'numeric',
    month: 'short',
    day: 'numeric',
  })
)
</script>
