<template>
  <img class="phone" src="~/assets/mobile/home-view-ios.png" />
</template>

<script>
export default {
  name: 'Phone',
}
</script>

<style>
.phone {
  @apply object-cover h-full;
  @apply absolute top-6;

  height: 105%;
}
</style>
