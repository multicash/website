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
  @apply mb-4 text-7xl text-black dark:text-white font-bold leading-none tracking-tight;
}
</style>
