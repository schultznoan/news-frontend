<template>
   <div class="wrapper">
      <ui-header />

      <RouterView />

      <ui-symbols />
   </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router';

import { UiHeader } from '@/widgets/header'
import { UiSymbols } from '@/shared/ui'
</script>