<template>
  <div class="menu-container">
    <div class="menu">
      <div class="menu-logo">
        <Logo flat />
      </div>

      <ul class="menu-links">
        <li v-for="page in pages" :key="page.name">
          <nuxt-link
            tag="a"
            :to="page.href"
            :class="{ primary: page.name === 'Download' }"
          >
            {{ page.name }}
          </nuxt-link>
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
          href: '/',
        },
        {
          name: 'Get Started',
          href: '/get-started',
        },
        {
          name: 'Download',
          href: '/',
        },
      ],
    },
  },
}
</script>

<style>
.menu-container {
  @apply bg-gray-100 dark:bg-black dark:bg-opacity-50;
}

.menu {
  @apply container mx-auto grid gap-4;
  @apply grid-cols-1 md:grid-cols-2;
  @apply py-4 px-10;
}

.menu-logo {
  @apply flex items-center;
  @apply justify-center md:justify-between;
}

.menu-logo svg {
  @apply w-auto h-5 md:h-7 lg:h-8;
}

.menu-links {
  z-index: 1;
  @apply flex align-middle md:m-2;
  @apply justify-center md:justify-end;
}

.menu-links li {
  @apply flex items-center;
}

.menu-links li a {
  @apply text-black dark:text-white hover:bg-white dark:hover:bg-black;
  @apply flex items-center justify-center font-bold cursor-pointer;
  @apply py-2 px-2 sm:py-3 sm:px-3 lg:px-5;
  @apply text-xs sm:text-sm lg:text-base;
  @apply rounded-md sm:rounded-lg;
}

.menu-links li a.primary {
  @apply relative bg-gray-100 dark:bg-gray-900 text-black dark:text-white font-bold;
  @apply py-1 px-1 sm:px-2 mx-2 lg:p-2 lg:mx-3;
  @apply text-sm sm:text-lg lg:text-xl;
  @apply rounded sm:rounded-lg;
}

.menu-links li a.primary::before {
  z-index: -1;
  content: '';
  @apply absolute bg-gradient-to-tr from-purple-600 via-purple-500 to-pink-500 -inset-1;
  @apply rounded-lg sm:rounded-xl;
}

.menu-links li a.primary:hover {
  z-index: 2;
  @apply bg-transparent text-white;
}
</style>
