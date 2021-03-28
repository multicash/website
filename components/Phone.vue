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
  @apply p-1
    bg-white
    dark:bg-gray-800
    rounded-2xl
    shadow-lg
    transform
    scale-200
    translate-y-20;
}

.phone img {
  @apply rounded-xl w-36;
}
</style>
