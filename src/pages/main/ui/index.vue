<template>
  <main class="main">
    <ui-banner :title="'Have you say'" />
    <section class="container offset section">
      <div class="section-selection">
        <news-search-widget class="section-selection__search" />
        <news-filter-widget class="section-selection_filter" />
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
import { UiBanner } from '@/shared/ui'

import { NewsSearchWidget, NewsFilterWidget } from '@/widgets/news'
</script>

<style lang="scss" scoped>
.section {
  &-selection {
    display: flex;
    align-items: center;
    justify-content: space-around;

    &__search {
      width: 70%;
    }
  }
}
</style>