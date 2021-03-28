<template>
  <div class="feature">
    <div class="feature-image">
      <svg
        class="h-12 w-12"
        :class="`text-${color}-500`"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
        />
      </svg>
    </div>
    <h4 :class="`text-${color}-500`">{{ title }}</h4>
    <p><slot /></p>
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

    color: {
      type: String,
      default: 'green',
    },
  },
}
</script>

<style>
.feature {
  @apply p-6 rounded-lg bg-gray-100 dark:bg-gray-800;
}

.feature-image {
  @apply flex;
}

.feature h4 {
  @apply font-bold text-2xl my-2;
}
</style>
