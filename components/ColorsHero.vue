<template>
  <div class="colors-hero">
    <container><slot /></container>
  </div>
</template>

<script>
export default {
  name: 'ColorsHero',
}
</script>

<style>
.colors-hero {
  @apply py-24 bg-colors;
}
</style>
