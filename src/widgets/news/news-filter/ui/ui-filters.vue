<template>
  <div v-if="filtersList.length" class="filters-list">
    <news-filter-block-widget v-for="filter in filtersList" :key="filter.id" :filter="filter" />
  </div>
</template>

<script setup>
import NewsFilterBlockWidget from './ui-filters-block.vue'
import { filtersList } from '../mocks'
</script>

<style lang="scss" scoped>
.filters-list {
  display: flex;
  align-items: center;
  width: 25%;
}
</style>