<script lang="ts" setup>
import {
  darkTheme,
  dateZhCN,
  zhCN,
} from 'naive-ui'

const color = useColorMode()

const theme = ref(color.value === 'light' ? null : darkTheme)
const themeOverrides = {
  common: {
    borderRadiusSmall: '4px',
    borderRadius: '6px',
  },
}

function changeTheme() {
  if (color.value === 'light') {
    theme.value = null
  }
  else if (color.value === 'dark') {
    theme.value = darkTheme
  }
}

watch(color, () => {
  changeTheme()
})
</script>

<template>
  <n-config-provider
    :locale="zhCN"
    :date-locale="dateZhCN"
    :theme="theme"
    :theme-overrides="themeOverrides"
  >
    <n-global-style />
    <n-loading-bar-provider>
      <n-dialog-provider>
        <n-notification-provider>
          <n-message-provider :max="1" placement="bottom">
            <slot />
          </n-message-provider>
        </n-notification-provider>
      </n-dialog-provider>
    </n-loading-bar-provider>
  </n-config-provider>
</template>
