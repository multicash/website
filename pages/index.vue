<template>
  <div>
    <!-- Header -->
    <div class="relative">
      <hero>
        <div class="header-container">
          <div>
            <p class="title">Get more.</p>
            <p class="subtitle">Spending, sending and saving<br />in minutes</p>
            <button class="button">Get started</button>
          </div>
          <div class="header-image">
            <img src="~/assets/mobile/home-view-ios.png" />
          </div>
        </div>
      </hero>
    </div>

    <div class="bg-colors p-8" />

    <!-- You're in control -->
    <div class="relative">
      <container class="youre-in-control-container">
        <div class="youre-in-control-image">
          <img src="~/assets/mobile/multicash-control-circle.png" />
        </div>
        <div class="youre-in-control-content">
          <BlockTitle>You're in control</BlockTitle>

          <div class="youre-in-control-features">
            <Feature
              title="Save"
              gradient-from="from-pink-400"
              gradient-to="to-pink-500"
            >
              Earn up to 2.50% APY interest.
            </Feature>
            <Feature
              title="Spend"
              gradient-from="from-pink-500"
              gradient-to="to-purple-500"
            >
              Easily pay for goods and services.
            </Feature>
            <Feature
              title="Control"
              gradient-from="from-green-500"
              gradient-to="to-blue-500"
            >
              Worldwide 24/7.
            </Feature>
          </div>

          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer
            adipiscing erat eget risus sollicitudin pellentesque et non erat.
          </p>

          <div class="flex justify-end">
            <button class="button">Learn more</button>
          </div>
        </div>
      </container>
    </div>

    <!-- It's simple -->
    <block class="bg-gray-100 dark:bg-gray-800 relative" large>
      <container>
        <BlockTitle from="from-purple-400" to="to-pink-500">
          It's simple
        </BlockTitle>

        <div class="simple-content">
          <div>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer
              adipiscing erat eget risus sollicitudin pellentesque et non erat.
              Maecenas nibh dolor, malesuada et bibendum a, sagittis accumsan
              ipsum. Pellentesque ultrices ultrices sapien, nec tincidunt nunc
              posuere ut. Lorem ipsum dolor sit amet, consectetur adipiscing
              elit. Nam scelerisque tristique dolor vitae tincidunt.
            </p>
            <button class="button">Get started</button>
          </div>
          <div class="simple-phones-image">
            <img src="~/assets/mobile/multicash-simple-phones.png" />
          </div>
        </div>
      </container>
    </block>

    <!-- Get Multi -->
    <div class="get-multi-block">
      <div class="get-multi-image">
        <img src="~/assets/multicash-get-multi.jpg" />
      </div>
      <container class="get-multi-container">
        <div>
          <logo flat inverted class="w-48" />
        </div>
        <p class="get-multi-title">Get multi</p>
      </container>
    </div>

    <div class="bg-colors h-4" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style>
.header-container {
  @apply grid gap-4;
  @apply grid-cols-1 md:grid-cols-2;
}

.title {
  @apply font-extrabold;
  @apply bg-clip-text text-transparent bg-gradient-to-r from-purple-500 to-pink-500;
  @apply text-6xl lg:text-8xl;
}

.subtitle {
  @apply font-extrabold;
  @apply bg-clip-text text-transparent bg-gradient-to-r from-purple-500 to-pink-500;
  @apply text-xl lg:text-2xl;
}

.header-image {
  @apply flex justify-center items-center;
  @apply -mt-14 md:mt-0;
}

.header-image img {
  @apply object-cover h-full;
  @apply relative md:absolute;
  @apply transform scale-100 md:scale-110 translate-y-24 md:translate-y-10;
}

.button {
  @apply ring-2 font-bold text-xl ring-black dark:ring-white rounded-lg p-2;
  @apply transition-all delay-200;
}

.button:hover {
  @apply bg-black dark:bg-white text-white dark:text-black;
  @apply transition-all delay-200;
}

.youre-in-control-container {
  @apply flex flex-col-reverse md:grid gap-10;
  @apply grid-cols-1 md:grid-cols-3;
}

.youre-in-control-image {
  @apply flex items-end justify-end;
}

.youre-in-control-image img {
  @apply object-right-bottom object-cover h-4/5;
  @apply relative md:absolute bottom-0;
}

.youre-in-control-content {
  @apply col-span-2 my-14 md:my-20;
}

.youre-in-control-features {
  @apply mt-8 grid grid-cols-1 md:grid-cols-3 gap-8;
}

.simple-content {
  @apply flex flex-col md:grid grid-cols-2 gap-10;
}

.simple-phones-image {
  @apply flex justify-center items-center;
}

.simple-phones-image img {
  @apply relative md:absolute bottom-0 h-full;
  @apply transform md:-translate-y-7;
}

.get-multi-block {
  @apply relative bg-purple-200;
}

.get-multi-container {
  @apply absolute inset-0;
  @apply flex flex-col items-center justify-between;
  @apply pt-6 pb-24;
}

.get-multi-image img {
  @apply h-screen max-h-full w-full object-cover object-top;
}

.get-multi-title {
  @apply font-bold text-white;
  @apply text-7xl md:text-9xl;
}
</style>
