<script lang="ts" setup>
import { options } from '@/constants/links'
</script>

<template>
  <n-dropdown trigger="hover" size="small" :options="options">
    <n-button type="tertiary" circle size="small">
      <template #icon>
        <n-icon class="i-ri-more-2-fill" />
      </template>
    </n-button>
  </n-dropdown>
</template>
