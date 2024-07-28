<template>
  <div class="banner">
    <svg width="40" height="40">
      <use xlink:href="#icon-home" />
    </svg>
    <h1>{{ title }}</h1>
  </div>
</template>

<script setup lang="ts">
const {
  title
} = defineProps({
  title: {
    type: String,
    required: true
  }
})
</script>