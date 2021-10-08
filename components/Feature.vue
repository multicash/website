<template>
  <div class="feature">
    <h4>
      <span
        class="bg-clip-text text-transparent bg-gradient-to-br"
        :class="[gradientFrom, gradientTo]"
      >
        {{ title }}
      </span>
    </h4>
    <p class="leading-none text-lg text-gray-500 dark:text-gray-200">
      <slot />
    </p>
  </div>
</template>

<script>
export default {
  name: 'Feature',

  props: {
    title: {
      type: String,
      default: '',
    },

    gradientFrom: {
      type: String,
      default: '',
    },

    gradientTo: {
      type: String,
      default: '',
    },
  },
}
</script>

<style>
.feature h4 {
  @apply font-black text-5xl;
}
</style>
