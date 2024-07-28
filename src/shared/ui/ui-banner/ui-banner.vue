<template>
  <section class="banner">
    <svg class="banner-icon" width="40" height="40">
      <use xlink:href="#icon-home" />
    </svg>
    <h1 class="banner-title">{{ title }}</h1>
  </section>
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

<style lang="scss" scoped>
.banner {
  text-align: center;
  padding-top: 70px;
  padding-bottom: 70px;
  background-color: var(--color-white);

  &-icon {
    margin-bottom: 15px;
  }

  &-title {
    font-size: 35px;
    font-weight: 600;
    color: var(--color-blue);
  }
}
</style>