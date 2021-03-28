<template>
  <div>
    <Menu />
    <Nuxt />
    <FooterLayout />
  </div>
</template>

<script>
import Menu from '~/layouts/Menu'
import FooterLayout from '~/layouts/FooterLayout'

export default {
  components: { FooterLayout, Menu },
}
</script>

<style>
html {
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  @apply bg-white dark:bg-gray-900 text-black dark:text-white;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
