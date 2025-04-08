<script >
defineProps({
  image: String,
  location: String,
  beach: String,
  rating: Number,
  highlight: Boolean
})
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/scss';
import 'swiper/scss/navigation';
import 'swiper/scss/pagination';

import './src/assets/style.scss';

// import required modules
import { FreeMode, Pagination } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [FreeMode, Pagination],
    };
  },
};
</script>

<template>
  <section id="hero">
    <div class="navbar">
      <div class="fixed w-full h-22  justify-center no-underline items-center-safe gap-6 flex important left-0 top-0 bg-transparent z-1">
        <h1 href="#" class=" left-10 absolute font-oswald text-4xl no-underline text-red-500 text-shadow-md">LP VIAGENS</h1>
        <div class="menu_list">
          <div>
            <ul id="nav_list" class="justify-center items-center-safe flex gap-20 important !no-underline text-red-500">
              <li class="relative text-shadow-lg text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a   href="#home">INICIO</a>
              </li>
              <li class="relative text-shadow-lg text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a href="#destinos"> DESTINOS DE PASSEIOS</a>
              </li>
              <li class="relative text-shadow-lg text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a href="#estadia">ESTADIA E POUSADAS</a>
              </li>
              <li class="relative text-shadow-lg text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a href="#voos">VOOS</a>
              </li>
            </ul>
          </div>
      </div>
    </div>
    </div>

  </section>
<main class="absolute h-13/10 w-full top-0 left-0 bg-[url('/fundo.jpg')] bg-cover">
  <div class="absolute top-40 left-96 h-100 flex w-150">
    <img src="../public/Switzerland Travel New.png" height="1368" width="1936"/>
    <h2 class="absolute top-70 text-center font-semibold animate-fade-in animation-delay-500 left-50% text-4xl text-shadow-lg">
      Venha conhecer o pais mais bonito do mundo</h2>
    <div>
    </div>
  </div>
</main>

  <main class="absolute justify-center font-semibold items-center-safe p-100% left-0 top-220 h-svh w-full bg-gray-300">
    <h2 class="absolute text-4xl text-red-500 opacity-100 left-20 top-9.5 ">DESTINOS DE PASSEIOS
      <div class="relative top-10 left-0 w-300 h-140 bg-gradient-to-b from-black/80 to-transparent ">
        <div class="">
          <swiper
              :slidesPerView="3"
              :spaceBetween="60"
              :freeMode="true"
              :pagination="{
      clickable: true,
    }"
              :modules="modules"
              class="mySwiper"
          >
            <swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide>
            <swiper-slide> <img src="/foto1.jpg" alt="Imagem 1"></swiper-slide><swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide>
            <swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide><swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide>
            <swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide><swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide>
            <swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide><swiper-slide><img src="/foto1.jpg" alt="Imagem 1"></swiper-slide>
          </swiper>
        </div>
      </div>
    </h2>
  </main>

  <main class="absolute justify-center font-semibold items-center-safe p-100% left-0 top-389 h-svh w-full bg-[url('fundo3.jpg')] opacity-85 bg-cover">
    <div class="rounded-xl absolute top-30 left-15 overflow-hidden shadow-lg w-64 bg-white">
      <div class="relative">
        <img src="/transferir-2.jpg" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Zurique - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 800,00</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-sm font-semibold">Bem avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-100 left-15 overflow-hidden shadow-lg w-64 h-64 bg-white">
      <div class="relative">
        <img src="/unnamed.jpg" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115"/>
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Zurique - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 659,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-sm font-semibold">Bem avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-100 left-95 overflow-hidden shadow-lg w-64  bg-white">
      <div class="relative">
        <img src="/761d26c3_original.jpg" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Genebra - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 600,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <!--<span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>-->
          <span class="text-yellow-500">★</span>
          <span class="text-sm font-semibold">Mal avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-100 left-175 overflow-hidden shadow-lg w-64 bg-white">
      <div class="relative">
        <img src="/FT4.avif" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Lucerna - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 300,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-sm font-semibold">Bem avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-100 left-255 overflow-hidden shadow-lg w-64 bg-white">
      <div class="relative">
        <img src="/FT6.avif" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Berna - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 1000,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-sm font-semibold">Bem avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-30 left-95 overflow-hidden shadow-lg w-64 bg-white">
      <div class="relative">
        <img src="/FT7.jpeg" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Zermatt - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 699,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-sm font-semibold">Bem avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-30 left-175 overflow-hidden shadow-lg w-64 bg-white">
      <div class="relative">
        <img src="/FT8.jpg" alt="Hotel" class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Zermatt - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 500,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <span class="text-white">★</span>
          <span class="text-sm font-semibold">Bem avaliado</span>
        </div>
      </div>
    </div>

    <div class="rounded-xl absolute top-30 left-255 overflow-hidden shadow-lg w-64 bg-white">
      <div class="relative">
        <img src="/FT9.avif" alt="Hotel"  class="w-full h-48 object-cover transition-transform duration-300 ease-in-out hover:scale-115" />
        <div v-if="highlight" class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
          🏆 Preferido dos hóspedes
        </div>
      </div>
      <div class="p-4">
        <h3 class="font-semibold text-gray-800">Montreux - Suiça</h3>
        <p class="text-sm text-gray-500">R$ 99,99</p>
        <div class="flex items-center gap-1 mt-2">
          <span class="text-yellow-500">★</span>
          <span class="text-yellow-500">★</span>
          <!-- <span class="text-yellow-500">★</span>-->
          <!-- <span class="text-yellow-500">★</span>
           <span class="text-yellow-500">★</span>-->
          <span class="text-sm font-semibold">Mal avaliado</span>
        </div>
      </div>
    </div>



    </main>
  <h2 class="absolute text-4xl font-semibold text-red-500 opacity-100 left-20 top-400.5 ">HOTEIS PARA SUA ESTADIA</h2>
</template>

<style scoped>
@import "tailwindcss";
* {
  padding: 0;
  margin: 0;
}

body {
  padding: 0;
  margin: 0;
}

</style>