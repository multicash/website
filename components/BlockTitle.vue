<template>
  <div class="block-title">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'BlockTitle',
}
</script>

<style>
.block-title {
  @apply text-black dark:text-white font-bold leading-none tracking-tight;
  @apply mb-4 text-6xl md:text-7xl;
}
</style>
