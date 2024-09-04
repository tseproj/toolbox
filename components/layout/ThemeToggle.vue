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

<template>
  <n-tooltip trigger="hover" :show-arrow="false">
    <template #trigger>
      <n-button type="tertiary" circle size="small" @click="toggleDark">
        <template #icon>
          <div v-if="color.value === 'dark'">
            <n-icon class="i-ri-moon-fill" />
          </div>
          <div v-if="color.value === 'light'">
            <n-icon class="i-ri-sun-fill" />
          </div>
        </template>
      </n-button>
    </template>
    <div v-if="color.value === 'dark'">
      切换到浅色模式
    </div>
    <div v-if="color.value === 'light'">
      切换到深色模式
    </div>
  </n-tooltip>
</template>

<style>

</style>
