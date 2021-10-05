<template>
  <div class="hero">
    <container><slot /></container>
  </div>
</template>

<script>
export default {
  name: 'Hero',
}
</script>

<style>
.hero {
  @apply py-24;
}
</style>
