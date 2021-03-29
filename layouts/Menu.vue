<template>
  <div class="menu-container">
    <div class="menu">
      <div class="menu-logo">
        <Logo class="w-auto h-7 sm:h-8" flat inverted />
      </div>

      <ul class="menu-links">
        <li v-for="page in pages" :key="page.name">
          <a>{{ page.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu',

  props: {
    pages: {
      type: Array,
      default: () => [
        {
          name: 'Home',
        },
        {
          name: 'Get Started',
        },
        {
          name: 'Download',
        },
      ],
    },
  },
}
</script>

<style>
.menu-container {
  @apply bg-colors;
}

.menu {
  @apply bg-white bg-opacity-10 grid grid-cols-2 gap-4;
}

.menu-logo {
  @apply ml-5 flex items-center;
}

.menu-links {
  @apply flex justify-end align-middle;
}

.menu-links li a {
  @apply p-5 flex items-center justify-center text-lg font-medium text-white hover:bg-white hover:bg-opacity-10 cursor-pointer;
}
</style>
