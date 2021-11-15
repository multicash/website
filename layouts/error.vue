<template>
  <hero>
    <div v-if="error.statusCode === 404" class="text-center">
      <h1 class="title">{{ error.statusCode }}</h1>
      <h2 class="text-6xl font-bold">{{ error.message }}</h2>
      <br />
      <br />
      <a href="/">Return home</a>
    </div>
  </hero>
</template>

<script>
import Hero from '~/components/Hero'

export default {
  components: { Hero },
  layout: 'error',

  props: {
    error: {
      type: Object,
      default: null,
    },
  },
}
</script>
