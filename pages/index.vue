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

    <block class="my-14">
      <container>
        <BlockTitle>What is MultiCash...</BlockTitle>

        <div class="mt-8 grid grid-cols-3 gap-8">
          <Feature class="transform -rotate-3 text-green-500" title="Save">
            Earn up to 2.50% APY interest on your digital currency holdings.
            That is 41.66x the average national savings account rate of 0.06%
            APY.
          </Feature>
          <Feature
            class="transform rotate-1 translate-y-11 text-yellow-500"
            title="Spend"
          >
            Easily pay for goods and services in a few seconds with no delays.
            Send and receive MultiCash from anywhere around the world.
          </Feature>
          <Feature
            class="transform rotate-3 text-blue-500"
            title="No Hidden Fees"
          >
            You don’t have to worry about account maintenance fees, or random
            hidden bank charges. The only thing you will see are transaction
            fees which are as a set 0.50%, just enough to ensure payments are
            delivered instantly.
          </Feature>
        </div>
      </container>
    </block>

    <block
      class="bg-gradient-to-bl from-blue-100 to-pink-200 dark:from-blue-900 dark:to-pink-900"
    >
      <container>
        <BlockTitle from="from-purple-400" to="to-pink-500">
          Who is MultiCash...
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
  @apply ring-2 font-bold text-lg ring-black rounded-lg p-2;
  @apply transition-all delay-200;
}

.button:hover {
  @apply bg-black text-white;
  @apply transition-all delay-200;
}
</style>
