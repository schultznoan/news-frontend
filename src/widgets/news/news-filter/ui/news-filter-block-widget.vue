<template>
  <div class="filters-block" @click.self="isFilterOpen = false">
    <div class="filters-block_icon" v-html="filter.icon" />
    <div class="filters-block_description" @click.stop="isFilterOpen = !isFilterOpen">
      <div>{{ filter.title }}</div>
      <div>
        <svg width="9" height="9">
          <use :xlink:href="isFilterOpen ? '#icon-up' : '#icon-down'" />
        </svg>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const {
  filter
} = defineProps({
  filter: {
    type: Object,
    required: true
  }
})

const isFilterOpen = ref(false)
</script>

<style lang="scss" scoped>
.filters-block {
  background-color: var(--color-white);
  width: 100%;
  display: flex;
  align-items: center;
  padding: 10px;
  border-radius: 10px;
  cursor: pointer;

  &:first-child {
    margin-right: 20px;
  }

  &_icon {
    margin-right: 5px;
  }

  &_description {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }
}
</style>