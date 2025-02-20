<template>
  <nav class="flex justify-between items-center px-4 py-3 bg-[#FFF1BE] shadow-md border-b-[1.5px] border-black">
    <div class="flex items-center space-x-2">
      <img src="~/assets/dish_full_fit.png" alt="Dish Icon" class="h-8" />
      <span class="text-xl font-bold">{{ siteName }}</span>
    </div>

    <div class="flex items-center space-x-[10.5px]">
      <button 
        class="flex items-center justify-center bg-gradient-to-br from-[#EB00FF] to-[#5BABFF] rounded-lg p-[5px] hover:opacity-80 transition-all"
        @click="openInNewTab('https://discord.gg/VDq4YvqrVg')"
      >
        <Icon name="ic:baseline-discord" class="text-[23px] cursor-pointer text-white" />
      </button>

      <button 
        class="flex items-center justify-center border-2 border-black rounded-lg p-[3px] hover:bg-gray-100 transition-all"
        @click="openInNewTab('https://github.com/downtomarsguy/generic-socionics-site')"
      >
        <Icon name="uil:github" class="text-[23px] cursor-pointer" />
      </button>

      <button 
        class="flex items-center justify-center border-2 border-black rounded-lg p-[3px] hover:bg-gray-100 transition-all"
        @click="toggleDarkMode"
      >
        <Icon :name="isDarkMode ? 'uil:moon' : 'uil:sun'" class="text-[23px] cursor-pointer" />
      </button>
    </div>
  </nav>
</template>

<script setup>
  import { ref, computed, onMounted, onBeforeUnmount } from 'vue';

  const isDarkMode = ref(false);
  const windowWidth = ref(0);
  const isClient = typeof window !== "undefined";

  const toggleDarkMode = () => {
    isDarkMode.value = !isDarkMode.value;
  };

  const openInNewTab = (url) => {
    window.open(url, "_blank");
  };

  const siteName = computed(() => {
    return windowWidth.value < 500 ? "GSS" : "Generic Socionics Site";
  });

  const handleResize = () => {
    if (isClient) {
      windowWidth.value = window.innerWidth;
    }
  };

  onMounted(() => {
    if (isClient) {
      windowWidth.value = window.innerWidth;
      window.addEventListener("resize", handleResize);
    }
  });

  onBeforeUnmount(() => {
    if (isClient) {
      window.removeEventListener("resize", handleResize);
    }
  });
</script>
