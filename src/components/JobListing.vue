<script setup>
import { ref, defineProps, computed } from 'vue'

const props = defineProps({
  job: Object,
})

const showFullDescription = ref(false)

const toggleFullDesc = () => {
  showFullDescription.value = !showFullDescription.value
}

const truncatedDesc = computed(() => {
  let description = props.job.description
  if (!showFullDescription.value) {
    description = description.substring(0, 20) + '...'
  }
  return description
})
</script>

<template>
  <div class="p-5 bg-gray-200 w-48 rounded-md">
    <h2>{{ props.job.title }}</h2>
    <p class="rounded-md bg-white p-2">{{ truncatedDesc }}</p>
    <button @click="toggleFullDesc" class="text-green-500 hover:text-green-600">
      {{ showFullDescription ? 'Less' : 'More' }}
    </button>
  </div>
</template>
