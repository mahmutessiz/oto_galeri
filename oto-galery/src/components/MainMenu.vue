<script setup>
import { RouterLink } from 'vue-router';
import DrawerMenu from './DrawerMenu.vue';

/**
 * !check if drawer element hidden or not, then take action accordingly
 */
const drawerMove = () => {
  const drawer = document.querySelector('#drawer-open-close');
  let isHidden = drawer.classList.contains('hidden');
  if (isHidden == true) {
    drawer.classList.remove('hidden');
    drawer.classList.remove('slide-to-right');
    drawer.classList.add('slide-to-left');
  } else {
    drawer.classList.add('hidden');
  }
};
</script>

<template>
  <section class="sticky top-0 z-20 w-full bg-white px-6 antialiased">
    <div class="mx-auto max-w-7xl">
      <nav class="relative z-50 h-24 select-none">
        <div
          class="container relative mx-auto flex h-24 flex-wrap items-center justify-between overflow-hidden border-b border-gray-200 font-medium sm:px-4 md:overflow-visible md:px-2 lg:justify-center"
        >
          <div class="flex h-full w-1/4 items-center justify-start pr-4">
            <RouterLink to="/" class="inline-block py-4 md:py-0">
              <img src="../assets/Arka_Plan.png" class="max-w-[7rem]" alt="ozbeyler auto logo" />
            </RouterLink>
          </div>
          <div
            class="left-0 top-0 hidden h-full w-full items-start bg-gray-900 bg-opacity-50 p-4 text-sm md:relative md:flex md:w-3/4 md:items-center md:bg-transparent md:p-0 lg:text-base"
          >
            <div
              class="h-auto w-full flex-col overflow-hidden rounded-lg bg-white md:relative md:flex md:flex-row md:overflow-visible md:rounded-none md:bg-transparent"
            >
              <div
                class="flex w-full flex-col items-start justify-center space-x-6 text-center md:mt-0 md:w-2/3 md:flex-row md:items-center lg:space-x-8"
              >
                <RouterLink
                  to="/"
                  class="mx-0 ml-6 inline-block w-full py-2 text-left font-medium text-indigo-600 md:mx-2 md:ml-0 md:w-auto md:px-0 md:text-center lg:mx-3"
                  >Anasayfa</RouterLink
                >
                <a
                  href="/"
                  class="mx-0 inline-block w-full py-2 text-left font-medium text-gray-700 hover:text-indigo-600 md:mx-2 md:w-auto md:px-0 md:text-center lg:mx-3"
                  >Ürünler</a
                >
                <RouterLink
                  to="/about"
                  class="mx-0 inline-block w-full py-2 text-left font-medium text-gray-700 hover:text-indigo-600 md:mx-2 md:w-auto md:px-0 md:text-center lg:mx-3"
                  >Hakkımızda</RouterLink
                >
                <RouterLink
                  to="/contact"
                  class="mx-0 inline-block w-full py-2 text-left font-medium text-gray-700 hover:text-indigo-600 md:mx-2 md:w-auto md:px-0 md:text-center lg:mx-3"
                  >İletişim</RouterLink
                >
              </div>
              <div
                class="flex w-full flex-col items-start justify-end pt-4 md:w-1/3 md:flex-row md:items-center md:py-0"
              >
                <RouterLink
                  to="/contact"
                  class="inline-flex w-full items-center bg-indigo-600 px-6 py-3 text-sm font-medium leading-4 text-white hover:bg-indigo-500 focus:outline-none focus:ring-0 focus:ring-indigo-600 focus:ring-offset-2 md:w-auto md:rounded-full md:px-3 md:focus:ring-2 lg:px-5"
                  >Bize ulaşın</RouterLink
                >
              </div>
            </div>
          </div>
          <div class="flex cursor-pointer md:hidden" @click="drawerMove">
            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
              <path fill="currentColor" d="M3 18v-2h18v2H3Zm0-5v-2h18v2H3Zm0-5V6h18v2H3Z" />
            </svg>
          </div>
        </div>
      </nav>
    </div>
  </section>

  <DrawerMenu id="drawer-open-close" class="hidden md:hidden" />
</template>

<style scoped>
.slide-to-left {
  animation: slide-move-left 300ms linear;
}

@keyframes slide-move-left {
  from {
    left: 120%;
  }
  to {
    left: 0%;
  }
}
</style>
