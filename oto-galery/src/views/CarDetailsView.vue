<template>
  <section>
    <div class="grid w-full grid-cols-12 place-content-center gap-4 px-4 md:pl-8 md:pr-0">
      <div class="col-span-12 h-96 bg-black/10 md:col-span-8"></div>
      <div class="hidden bg-green-500/10 px-4 py-4 text-center md:col-span-3 md:block">
        <h2 class="pb-4 font-bold">İletişim</h2>
        <ul class="px-3 pb-4 text-left">
          <li class="border-b pt-2">Bizi arayın: 690690696</li>
          <li class="border-b pt-2">WhatsApp: 690690696</li>
          <li class="border-b pt-2">Facebook</li>
          <li class="border-b pt-2">instagram</li>
          <li class="border-b pt-2">e-mail:</li>
        </ul>
        <!-- harita bilgisi -->
        <h2 class="pb-4 font-bold">Harita Bilgisi</h2>
        <div class="relative overflow-hidden">
          <a
            href="https://yandex.com.tr/harita/101474/konya/?utm_medium=mapframe&utm_source=maps"
            style="color: #eee; font-size: 12px; position: absolute; top: 0px"
            >Konya</a
          ><a
            href="https://yandex.com.tr/harita/101474/konya/?ll=32.492129%2C37.874904&utm_medium=mapframe&utm_source=maps&z=12"
            style="color: #eee; font-size: 12px; position: absolute; top: 14px"
            >Yandex Maps: Ulaşım, navigasyon, yer arama</a
          ><iframe
            src="https://yandex.com.tr/map-widget/v1/?ll=32.492129%2C37.874904&z=12"
            class="aspect-square w-full"
            frameborder="1"
            allowfullscreen="true"
            style="position: relative"
          ></iframe>
        </div>
        <!-- maps end -->
      </div>
    </div>
  </section>
</template>
