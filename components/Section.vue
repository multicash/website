<template>
  <section class="section">
    <slot />
  </section>
</template>

<script>
export default {
  name: 'Section',
}
</script>

<style>
.section {
  @apply py-16;
}
</style>
