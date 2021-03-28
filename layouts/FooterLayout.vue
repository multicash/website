<template>
  <footer class="footer">
    <container>
      <div class="grid grid-cols-4 gap-6">
        <div v-for="section in sections" :key="section.name">
          <h6 class="footer-link-title">{{ section.name }}</h6>
          <ul>
            <li
              v-for="link in section.links"
              :key="link.name"
              class="footer-link"
            >
              <a>{{ link.name }}</a>
            </li>
          </ul>
        </div>
      </div>

      <Logo class="w-auto h-7 sm:h-8" />

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
            },
            {
              name: 'Documentation',
            },
            {
              name: 'GitBook',
            },
            {
              name: 'Contact Us',
            },
          ],
        },
        {
          name: 'Get Started',
          links: [
            {
              name: 'Wallets',
            },
            {
              name: 'Exchanges',
            },
            {
              name: 'Block Explorer',
            },
            {
              name: 'Media Kit',
            },
          ],
        },
        {
          name: 'Project',
          links: [
            {
              name: 'GitHub',
            },
            {
              name: 'Privacy Policy',
            },
          ],
        },
        {
          name: 'Community',
          links: [
            {
              name: 'Twitter',
            },
            {
              name: 'Discord',
            },
            {
              name: 'Reddit',
            },
            {
              name: 'Facebook',
            },
            {
              name: 'Telegram',
            },
            {
              name: 'Bitcointalk',
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

.footer-link-title {
  @apply font-bold text-xl mb-2 text-purple-900 dark:text-purple-400;
}

.footer-link {
  @apply py-1 hover:text-blue-400 cursor-pointer;
}

.copyright {
  @apply text-gray-500 mt-4;
}
</style>
