<!-- This is the example of a wrapper component -->
<script setup>
import { defineProps } from 'vue';

defineProps({
  bg: {
    type: String,
    default: 'bg-green-300'
  }
});
</script>

<template>
  <div :class="`${bg} shadow-md rounded-lg p-6 max-w-max my-2`">
    <slot></slot>
  </div>
</template>