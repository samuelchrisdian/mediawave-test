<script setup>
import Navbar from '~/components/_navbar.vue'
import Footer from '~/components/_footer.vue'
import Hero from '~/components/_hero.vue'
import Leaflet from '~/components/_leaflet.vue'
import Chart from '~/components/_chart.vue'

useHead({
  title: 'Samuel Chrisdian - MediaWave Recruitment Test',
  link: [
    { rel: 'icon', href: 'https://mediawave.id/assets/logo-black.png' }
  ]
})

const colorMode = useColorMode()
</script>

<template>
  <div class="bg-white">
    <Navbar />
    <Hero />
    <Leaflet />
    <Chart />
    <NuxtPage class="mx-auto p-4" />
    <Footer />
  </div>
</template>

<style lang="postcss">
body {
  @apply min-h-screen bg-white dark:bg-gray-800 dark:text-gray-200;
}
</style>
