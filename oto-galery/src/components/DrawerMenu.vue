<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="fixed z-20 -mt-4 h-screen w-full bg-white pt-4">
    <ul class="flex w-full flex-wrap">
      <li
        class="w-full cursor-pointer bg-gray-100 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-500"
      >
        <RouterLink to="/"><p class="w-full">Anasayfa</p></RouterLink>
      </li>

      <li
        class="w-full cursor-pointer bg-gray-200 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-300"
      >
        <p class="w-full">Ürünler</p>
      </li>
      <li
        class="w-full cursor-pointer bg-gray-100 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-500"
      >
        <RouterLink to="/about"><p class="w-full">Hakkımızda</p></RouterLink>
      </li>
      <li
        class="w-full cursor-pointer bg-gray-200 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-300"
      >
        <RouterLink to="/contact"><p class="w-full">İletişim</p></RouterLink>
      </li>
    </ul>
  </div>
</template>
