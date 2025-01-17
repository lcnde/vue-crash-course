<script setup>
import Card from '../components/Card.vue'
import JobListings from '../components/JobListings.vue'
import jobData from '../jobs.json'
</script>

<template>
  <h1 class="text-3xl">My vue app</h1>
  <button @click="clickMe">Click me</button>
  <Card>
    <h2 class="text-xl">Card title</h2>
    <p class="text-gray-600">Card content</p>
  </Card>
  <Card bg="bg-red-300">
    <h2 class="text-xl">Card title</h2>
    <p class="text-gray-600">Card content</p>
  </Card>
  <JobListings :jobs="jobData" />
</template>
