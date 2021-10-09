<template>
  <div class="menu-container">
    <div class="menu">
      <div class="menu-logo">
        <Logo class="w-auto h-7 sm:h-8" flat />
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
  @apply container mx-auto py-4 px-10 grid grid-cols-2 gap-4;
}

.menu-logo {
  @apply flex items-center;
}

.menu-links {
  z-index: 1;
  @apply flex justify-end align-middle;
}

.menu-links li {
  @apply flex items-center;
}

.menu-links li a {
  @apply text-black dark:text-white hover:bg-white dark:hover:bg-black;
  @apply p-5 flex items-center justify-center text-base font-bold cursor-pointer;
}

.menu-links li a.primary {
  @apply relative bg-gray-100 dark:bg-gray-900 text-xl text-black dark:text-white font-bold rounded-lg;
  @apply transition-all delay-200;
  @apply p-2 mx-3;
}

.menu-links li a.primary::before {
  z-index: -1;
  content: '';
  @apply absolute bg-gradient-to-tr from-purple-600 via-purple-500 to-pink-500 -inset-1 rounded-xl;
}

.menu-links li a.primary:hover {
  z-index: 2;
  @apply bg-transparent text-white;
}
</style>
