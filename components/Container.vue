<template>
  <div class="main-container"><slot /></div>
</template>

<script>
export default {
  name: 'Container',
}
</script>

<style>
.main-container {
  @apply container mx-auto px-4 sm:px-10;
}
</style>
