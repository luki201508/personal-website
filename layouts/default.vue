<template>
  <div
    class="
      w-full
      h-full
      flex flex-col
      justify-between
      items-center
      dark:bg-gray-900
    "
  >
    <Navbar />
    <div class="-mt-16 -mb-20 w-3/4 h-screen">
      <Nuxt />
    </div>
    <Footer />
    <DarkMode />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
