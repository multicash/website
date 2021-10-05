<template>
  <div class="phone">
    <img src="~/assets/mobile/home-view-ios.png" />
  </div>
</template>

<script>
export default {
  name: 'Phone',
}
</script>

<style>
.phone {
  @apply absolute
    p-1
    bg-white
    dark:bg-gray-800
    rounded-2xl
    shadow-lg
    transform
    scale-150
    translate-y-14;
}

.phone img {
  @apply rounded-xl w-32;
}
</style>
