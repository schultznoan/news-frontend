<template>
   <div class="wrapper">
      <header-widget />

      <RouterView />

      <ui-symbols />
   </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router';

import { HeaderWidget } from '@/widgets/header'
import { UiSymbols } from '@/shared/ui'
</script>