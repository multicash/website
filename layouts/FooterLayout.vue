<template>
  <footer class="footer">
    <container>
      <div class="footer-content">
        <div v-for="section in sections" :key="section.name">
          <h6 class="footer-link-title">{{ section.name }}</h6>
          <ul>
            <li
              v-for="link in section.links"
              :key="link.name"
              class="footer-link"
            >
              <a :href="link.href">{{ link.name }}</a>
            </li>
          </ul>
        </div>
      </div>

      <Logo class="w-auto h-7 sm:h-8" flat />

      <div class="copyright">© 2021 MultiCash. All Rights Reserved</div>
    </container>
  </footer>
</template>

<script>
export default {
  name: 'FooterLayout',

  data() {
    return {
      sections: [
        {
          name: 'Learn',
          links: [
            {
              name: 'About MultiCash',
              href: '/',
            },
            {
              name: 'Documentation',
              href: 'https://github.com/multicash',
            },
            {
              name: 'Contact Us',
              href: '/contact',
            },
          ],
        },
        {
          name: 'Get Started',
          links: [
            {
              name: 'Downloads',
              href: '/download',
            },
            {
              name: 'Buy MultiCash',
              href: '/buy',
            },
            {
              name: 'Transaction Details',
              href: 'https://explorer.multicash.io',
            },
            {
              name: 'Media Kit',
              href: '/media-kit',
            },
          ],
        },
        {
          name: 'Project',
          links: [
            {
              name: 'GitHub',
              href: 'https://github.com/multicash',
            },
            {
              name: 'Privacy Policy',
              href: '/privacy-policy',
            },
          ],
        },
        {
          name: 'Community',
          links: [
            {
              name: 'Twitter',
              href: 'https://twitter.com/MultiCash_io',
            },
            {
              name: 'Discord',
              href: 'https://discord.gg/eYQSkb9VJU',
            },
          ],
        },
      ],
    }
  },
}
</script>

<style>
.footer {
  @apply py-10 bg-gray-100 dark:bg-gray-800 text-gray-700 dark:text-gray-500;
}

.footer-content {
  @apply grid grid-cols-2 md:grid-cols-4 gap-6 pb-5;
}

.footer-link-title {
  @apply font-bold text-xl mb-2 text-purple-900 dark:text-purple-400;
}

.footer-link {
  @apply py-1 hover:text-blue-400 cursor-pointer;
}

.footer .multicash-logo {
  @apply mt-5 md:mt-0;
}

.copyright {
  @apply text-gray-500 mt-4;
}
</style>
