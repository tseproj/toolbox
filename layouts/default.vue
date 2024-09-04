<script lang="ts" setup>

</script>

<template>
  <n-layout position="absolute">
    <n-layout-header bordered class="sticky top-0 z40 h13 w-full flex items-center backdrop-blur-xl backdrop-filter">
      <nav px="5" class="relative mxauto w-full flex items-center justify-between gap-x-5">
        <div class="min-w-max flex items-center">
          <nuxt-link to="/" class="relative flex items-center gap-2.5">
            <span inline-flex text-lg font-black>
              h2B
            </span>
          </nuxt-link>
        </div>
        <div
          lg="top-0 relative w-max flex"
          class="absolute left-0 top-full w-full gap-x-6 duration-300 ease-linear transition-none"
        >
          <div mt="10 lg:0" class="min-w-max flex flex-col gap-2 sm-flex-row sm-items-center">
            <LayoutThemeToggle />
            <LayoutLinkDropdown />
          </div>
        </div>
      </nav>
    </n-layout-header>
    <slot />
  </n-layout>
</template>

<style>

</style>
