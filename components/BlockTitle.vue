<template>
  <div class="mb-4 text-5xl font-extrabold leading-none tracking-tight">
    <span
      class="bg-clip-text text-transparent bg-gradient-to-r"
      :class="[from, to]"
    >
      <slot />
    </span>
  </div>
</template>

<script>
export default {
  name: 'BlockTitle',

  props: {
    from: {
      type: String,
      default: 'from-green-400',
    },
    to: {
      type: String,
      default: 'to-blue-500',
    },
  },
}
</script>
