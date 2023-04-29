<script setup>
import { useRoute } from 'vue-router';
import Cardata from '../data/carData.json';

const route = useRoute();
const carId = route.params.id;

const carData = Cardata;
</script>
<template>
  <section>
    <div class="grid w-full grid-cols-12 place-content-center gap-2 px-4 md:pl-8 md:pr-0">
      <div class="col-span-12 flex flex-wrap md:col-span-8">
        <!-- car details -->
        <div class="flex w-full" v-for="car in carData.cars" :key="car.id">
          <div class="flex w-full flex-wrap" v-if="car.id == carId">
            <div class="w-full py-4">
              image carousel <br />
              <img src="../assets/hero-img.png" alt="" />
            </div>
            <ul class="flex w-full flex-wrap items-end">
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">İsim: &nbsp;</span> {{ car.isim }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">İlan Tarihi: &nbsp;</span> {{ car['İlan Tarihi'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">Yıl: &nbsp;</span> {{ car['Yıl'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Yakıt: &nbsp;</span> {{ car['Yakıt'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Vites: &nbsp;</span> {{ car['Vites'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">Araç Durumu: &nbsp;</span> {{ car['Araç Durumu'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">KM: &nbsp;</span> {{ car['KM'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Kasa tipi: &nbsp;</span> {{ car['Kasa Tipi'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Motor Gücü: &nbsp;</span> {{ car['Motor Gücü'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">Motor Hacmi: &nbsp;</span> {{ car['Motor Hacmi'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">Çekiş: &nbsp;</span> {{ car['Çekiş'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Renk: &nbsp;</span> {{ car['Renk'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Garanti: &nbsp;</span> {{ car['Çekiş'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">Ağır Hasar Kayıtlı: &nbsp;</span>
                {{ car['Ağır Hasar Kayıtlı'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-100">
                <span class="font-bold">Plaka / Uyruk: &nbsp;</span> {{ car['Plaka / Uyruk'] }}
              </li>
              <li class="w-full bg-slate-100 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Kimden: &nbsp;</span> {{ car['Kimden'] }}
              </li>
              <li class="w-full bg-slate-200 py-4 pl-4 md:w-1/2 md:bg-slate-200">
                <span class="font-bold">Fiyat: &nbsp;</span> {{ car['Fiyat'] }}
              </li>
            </ul>
            <!-- car about -->

            <div class="w-full border-t border-black/80 px-4 py-4">
              <h3 class="py-4 text-center text-xl font-bold">Açılama</h3>
              <p>
                {{ car['kisa-aciklama'] }}
              </p>
              <br />
              <p>
                Daha fazla bilgi için: <br />
                iletişim bölümü
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- iletişim -->
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
        <!-- maps end -->
      </div>
    </div>
  </section>
</template>
