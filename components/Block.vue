<template>
  <div class="py-16" :class="{ 'py-24': large }">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'Section',

  props: {
    large: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
