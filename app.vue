<script setup lang="ts">
useHead({
  titleTemplate: (page) => {
    return page ? `${page} | 氢量` : '氢量'
  },
})

// const themeRef = ref< GlobalTheme | null> (darkTheme)
// const darkThemeOverrides: GlobalThemeOverrides = {
//   common: {
//     borderRadiusSmall: '4px',
//     borderRadius: '6px',
//   },
// }
// const lightThemeOverrides: GlobalThemeOverrides = {
//   common: {
//     borderRadiusSmall: '4px',
//     borderRadius: '6px',
//   },
// }
</script>

<template>
  <Provider>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </Provider>
</template>

<style>
*::-webkit-scrollbar {
  display: none;
}

a {
  color: var(--n-text-color);
}

.n-dropdown-menu {
  user-select: none;
}

.n-popover__content {
  white-space: pre-line;
  user-select: none;
  max-width: 75vw;
}

.n-dialog .n-dialog__content {
  white-space: pre-line;
}

img {
  -webkit-user-drag: none;
}

.flexCenter {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>

<style scoped>
* {
  user-select: none;
}
</style>
