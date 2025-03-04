<template>
  <div class="bg-[#FFF6D4] min-h-screen">
    <Navbar />
    <div class="mt-16 sm:mt-4 md:mt-20 lg:mt-28 mx-4 sm:mx-8 md:mx-16">
      <p class="text-4xl sm:text-5xl md:text-6xl font-bold leading-tight">
        A 
        <span class="bg-clip-text leading-tight text-transparent bg-gradient-to-r from-[#EB00FF] to-[#5BABFF]">
          perpetually evolving
        </span>
        Socionics website
      </p>
      <p class="text-base sm:text-lg md:text-xl mt-4 max-w-4xl">
        Welcome to Yet Another Generic Socionics Site. The website will hold discussions on various schools such as Model A, Model G, Classical Socionics (SCS), Western Socionics (SWS) etc etc. The point of the site is to foster a collection of resources and guides for newcomers who are ready to learn about Socionics.
      </p>
      <div class="pt-4 space-x-4 flex">
        <button class="bg-gradient-to-r from-[#EB00FF] to-[#5BABFF] text-white py-2 rounded-md font-bold shadow-md hover:opacity-80 transition duration-300 text-lg w-48">
          Join Discord
        </button>
        <button class="border-2 border-black text-black py-2 rounded-md font-bold hover:bg-black hover:text-white transition duration-300 text-lg w-48 outline-2 outline-black outline-offset-2">
          Explore
        </button>
      </div>
      <div class="pb-10"></div>
    </div>
  </div>
</template>

<script setup>
  import Navbar from "~/components/Navbar.vue";
</script>
