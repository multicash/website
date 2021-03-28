<template>
  <div
    class="p-10 my-10 bg-white dark:bg-gray-800 shadow-xl rounded-lg flex gap-8"
  >
    <img
      v-if="img"
      class="w-48 h-48 rounded-full object-cover"
      :src="require(`~/assets/persons/${img}`)"
      :alt="`Picture of ${name}`"
    />
    <div>
      <h4 class="font-bold text-xl text-pink-500">{{ name }}</h4>
      <h6 class="font-medium text-lg">{{ title }}</h6>
      <p class="text-gray-500">{{ email }}</p>
      <p class="mt-4 text-gray-900 dark:text-gray-100">
        <slot />
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Person',

  props: {
    name: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
    email: {
      type: String,
      default: '',
    },
    img: {
      type: String,
      default: null,
    },
  },
}
</script>
