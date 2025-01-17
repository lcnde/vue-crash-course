<script setup>
import { defineProps } from 'vue'
import JobListing from './JobListing.vue'

const props = defineProps({
  jobs: Array,
})

console.log(props.jobs)

// const jobs = ref(jobData)
</script>

<template>
  <div class="p-5">
    <h1 class="text-3xl">Job Listing</h1>
    <div class="grid grid-cols-3 py-5 justify-items-center">
      <JobListing v-for="job in props.jobs" :key="job.id" :job="job" />
    </div>
  </div>
</template>
