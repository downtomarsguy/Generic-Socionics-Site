<template>
    <nav class="flex justify-between items-center p-4 bg-[#FFF1BE] shadow-md">
      <div class="flex items-center space-x-2">
        <img src="~/assets/dish_full_fit.png" alt="Dish Icon" class="h-8" />
        <span class="text-xl font-bold">Generic Socionics Site</span>
      </div>
    </nav>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isDarkMode = ref(false);
  
  const toggleDarkMode = () => {
    isDarkMode.value = !isDarkMode.value;
  };
  </script>