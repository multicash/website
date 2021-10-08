<template>
  <div>
    <hero>
      <div class="grid grid-cols-2 gap-4">
        <div>
          <p class="title">Get more.</p>
          <p class="subtitle">Spending, sending and saving<br />in minutes</p>
          <button class="button">Get started</button>
        </div>
        <div class="flex justify-center items-end relative">
          <phone />
        </div>
      </div>
    </hero>
    <div class="bg-colors p-8" />

    <div class="relative">
      <container class="grid grid-cols-3 gap-8">
        <div class="flex items-end justify-end">
          <img
            src="~/assets/mobile/hand-phone.png"
            class="youre-in-control-image"
          />
        </div>
        <div class="col-span-2 my-20">
          <BlockTitle>You're in control</BlockTitle>

          <div class="mt-8 grid grid-cols-3 gap-8">
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

    <block
      class="bg-gradient-to-bl from-blue-100 to-pink-200 dark:from-blue-900 dark:to-pink-900"
    >
      <container>
        <BlockTitle from="from-purple-400" to="to-pink-500">
          It's simple
        </BlockTitle>

        <div class="grid grid-cols-3">
          <Person
            class="col-span-2 transform -rotate-2"
            name="Jay Sanders"
            title="Founder & CEO"
            email="sanders@multicash.io"
            img="jay-sanders-1.jpg"
          >
            Jay Sanders is a zealous Tech-Enthusiast and IT Expert who shares an
            incredible passion for innovation and technology. He is the founder
            and CEO of MultiCash and is a professional who aspires to inspire a
            positive change in the community by leveraging the power of
            technology. Based in Lexington, Kentucky, Jay has always been
            enthused by the idea of using innovative technology to shape lives.
            He is an avid seeker of knowledge who strives for excellence in
            every facet of life. Jay’s passion for technology and love for
            community service inspired him to formulate MultiCash - An
            innovative digital currency designed to simplify money management
            and digital banking.
          </Person>

          <Person
            class="col-start-2 col-span-2 transform rotate-1"
            name="Swen van Zanten"
            title="Software Developer"
            email="swen@multicash.io"
            img="swen-van-zanten-1.jpg"
          >
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer
            adipiscing erat eget risus sollicitudin pellentesque et non erat.
            Maecenas nibh dolor, malesuada et bibendum a, sagittis accumsan
            ipsum. Pellentesque ultrices ultrices sapien, nec tincidunt nunc
            posuere ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            Nam scelerisque tristique dolor vitae tincidunt.
          </Person>
        </div>
      </container>
    </block>

    <block>
      <container>
        <BlockTitle from="from-yellow-400" to="to-red-500">
          Get Started!
        </BlockTitle>

        <p class="text-gray-900 dark:text-gray-100">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer
          adipiscing erat eget risus sollicitudin pellentesque et non erat.
          Maecenas nibh dolor, malesuada et bibendum a, sagittis accumsan ipsum.
          Pellentesque ultrices ultrices sapien, nec tincidunt nunc posuere ut.
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam
          scelerisque tristique dolor vitae tincidunt.
        </p>
        <p class="text-gray-900 dark:text-gray-100">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer
          adipiscing erat eget risus sollicitudin pellentesque et non erat.
          Maecenas nibh dolor, malesuada et bibendum a, sagittis accumsan ipsum.
        </p>
      </container>
    </block>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style>
.title {
  @apply text-8xl font-extrabold;
  @apply bg-clip-text text-transparent bg-gradient-to-r from-purple-500 to-pink-500;
}

.subtitle {
  @apply text-2xl font-extrabold;
  @apply bg-clip-text text-transparent bg-gradient-to-r from-purple-500 to-pink-500;
}

.button {
  @apply ring-2 font-bold text-xl ring-black rounded-lg p-2;
  @apply transition-all delay-200;
}

.button:hover {
  @apply bg-black text-white;
  @apply transition-all delay-200;
}

.youre-in-control-image {
  @apply object-right-bottom object-cover h-4/5;
  @apply absolute bottom-0;
}
</style>
