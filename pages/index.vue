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
      <p class="text-base sm:text-lg md:text-xl mt-4 max-w-4xl pb-10">
        Welcome to Yet Another Generic Socionics Site. This is a website for all Socionics related discussions. The site encompasses information from various schools but emphasizes Model A (SCS) & Model G (Gulenko). This website is for both people who are extremely familiar with Socionics as well as people who are simply learning about the theory.
      </p>
    </div>
  </div>
</template>

<script setup>
  import Navbar from "~/components/Navbar.vue";
</script>
