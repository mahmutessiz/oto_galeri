<script setup>
import { RouterLink } from 'vue-router';

/**
 * ! Close the drawer
 */

function deneme() {
  const drawerChild = document.querySelector('#drawer-open-close');
  drawerChild.classList.add('hidden');
}
</script>

<template>
  <div
    class="fixed z-20 -mt-4 hidden h-screen w-full bg-white/50 pt-4 backdrop-blur-lg"
    @click="deneme"
  >
    <ul class="flex w-full flex-wrap">
      <li
        class="w-full cursor-pointer border border-b border-black/20 bg-gray-100/40 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-500"
        @click="deneme"
      >
        <RouterLink to="/"><p class="w-full">Anasayfa</p></RouterLink>
      </li>

      <li
        class="w-full cursor-pointer border border-b border-black/20 bg-gray-200/40 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-300"
        @click="deneme"
      >
        <p class="w-full">Ürünler</p>
      </li>
      <li
        class="w-full cursor-pointer border border-b border-black/20 bg-gray-100/40 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-500"
        @click="deneme"
      >
        <RouterLink to="/about"><p class="w-full">Hakkımızda</p></RouterLink>
      </li>
      <li
        class="w-full cursor-pointer border border-b border-black/20 bg-gray-200/40 py-3 text-center text-xl transition-all duration-200 hover:bg-rose-300"
        @click="deneme"
      >
        <RouterLink to="/contact"><p class="w-full">İletişim</p></RouterLink>
      </li>
    </ul>
    <div class="mt-12 flex w-full items-center justify-center">
      <img src="../assets/arka_plan.png" class="w-full opacity-40" alt="ozbeyler auto logo" />
    </div>
  </div>
</template>
