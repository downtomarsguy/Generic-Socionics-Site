<template>
  <div class="bg-[#FFF6D4] h-screen">
    <Navbar />
    <slot />
  </div>
</template>

<script setup>
  import Navbar from '~/components/Navbar.vue';
</script>