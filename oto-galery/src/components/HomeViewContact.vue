<template>
  <section class="mt-12 flex w-full flex-wrap items-center justify-center py-4">
    <h2 class="pb-8 text-2xl font-bold">Harita ve Adres Bilgisi</h2>
    <div class="flex w-full flex-wrap justify-center gap-2">
      <!-- harita bilgisi -->
      <div class="relative w-1/3 min-w-[20rem] max-w-[30rem] overflow-hidden">
        <a
          href="https://yandex.com.tr/harita/101474/konya/?utm_medium=mapframe&utm_source=maps"
          style="color: #eee; font-size: 12px; position: absolute; top: 0px"
          >Konya</a
        ><a
          href="https://yandex.com.tr/harita/101474/konya/?ll=32.492129%2C37.874904&utm_medium=mapframe&utm_source=maps&z=12"
          style="color: #eee; font-size: 12px; position: absolute; top: 14px"
          >Yandex Maps: Ulaşım, navigasyon, yer arama</a
        >
        <iframe
          src="https://yandex.com.tr/map-widget/v1/?ll=32.492129%2C37.874904&z=12"
          class="aspect-square w-full"
          frameborder="1"
          allowfullscreen="true"
          style="position: relative"
        ></iframe>
      </div>

      <!-- Contact info -->
      <ul class="w-1/3 min-w-[20rem] px-4 py-4">
        <li class="pb-2"><span class="font-bold">Telefon:</span> 0545 323 73 68</li>
        <li class="pb-2"><span class="font-bold">WhatsApp:</span> 0545 323 73 68</li>
        <li class="pb-2"><span class="font-bold">E-posta:</span> ozauto@gmail.com</li>
        <li class="pb-2">
          <span class="font-bold">Adres:</span> bilmemne mh. sanayi sitesi no:15 vhsj auto
          çumra/konya
        </li>
      </ul>
    </div>
  </section>
</template>
