<template>
  <n-button type="tertiary" circle @click="toggleDark">
    <template #icon>
      <n-icon class="i-ri-sun-fill dark:i-ri-moon-fill" />
    </template>
  </n-button>
</template>

<script lang="ts" setup>
const color = useColorMode()

useHead({
  meta: [{
    id: 'theme-color',
    name: 'theme-color',
    content: () => color.value === 'dark' ? '#222222' : '#ffffff',
  }],
})

function toggleDark() {
  color.preference = color.value === 'dark' ? 'light' : 'dark'
}
</script>

<style>

</style>