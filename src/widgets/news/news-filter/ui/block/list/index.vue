<template>
  <div
    v-if="filtersList?.length"
    class="filters-block__list"
  >
    <!-- <div v-for="filter in filtersList" :key="filter.id">
      {{ filter.title }}
    </div> -->
  </div>
  <div v-else>
    Фильтры отсутствуют
  </div>
</template>

<script setup lang="ts">
defineProps({
  filtersList: {
    type: Array,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.filters-block__list {
  background: linear-gradient(90deg,
      rgba(102, 136, 255, 0.1) 0%,
      rgba(105, 102, 255, 0.1) 100%);
  backdrop-filter: blur(4px);
  border-radius: 0px 0px 10px 10px;
  padding: 10px 30px;
  width: 100%;
  position: absolute;
}
</style>