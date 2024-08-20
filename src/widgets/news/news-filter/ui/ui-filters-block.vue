<template>
  <div class="filters-block" @click.stop="isFilterOpen = !isFilterOpen">
    <div class="filters-block__content">
      <div class="filters-block__content-icon" v-html="filter.icon" />
      <div class="filters-block__content-description">
        <div>{{ filter.title }}</div>
        <div>
          <svg width="9" height="9">
            <use :xlink:href="isFilterOpen ? '#icon-up' : '#icon-down'" />
          </svg>
        </div>
      </div>
    </div>
    <ui-filters-block-list v-if="isFilterOpen" :filters-list="filter.list" />
  </div>
</template>

<script setup>
import UiFiltersBlockList from './ui-filters-block-list.vue'
import { ref } from 'vue'

defineProps({
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
  border-radius: 10px;
  width: 100%;
  cursor: pointer;
  position: relative;

  &:first-child {
    margin-right: 20px;
  }

  &__content {
    display: flex;
    align-items: center;
    width: 100%;
    padding: 10px;

    &-icon {
      margin-right: 5px;
    }

    &-description {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
    }
  }
}
</style>