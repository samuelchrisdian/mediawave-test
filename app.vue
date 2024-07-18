<script setup>
import Navbar from '~/components/_navbar.vue'

const colorMode = useColorMode()
</script>

<template>
  <div>
    <Navbar />
    <NuxtPage class="mx-auto p-4" />
  </div>
</template>

<style lang="postcss">
body {
  @apply min-h-screen bg-white dark:bg-gray-800 dark:text-gray-200;
}
</style>
