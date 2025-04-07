<script setup>

</script>

<template>
  <section id="hero">
    <div class="navbar">
      <div class="fixed w-full h-22  justify-center no-underline items-center-safe gap-6 flex important left-0 top-0 bg-black z-1">
        <a href="#" class="text-gray-500 left-10 absolute font-mono text-4xl no-underline">LP VIAGENS</a>
        <div class="menu_list">
          <div>
            <ul id="nav_list" class="justify-center items-center-safe flex gap-20 important !no-underline text-red-500">
              <li class="relative text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a   href="#home">INICIO</a>
              </li>
              <li class="relative text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a href="#bio"> DESTINOS DE PASSEIOS</a>
              </li>
              <li class="relative text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a href="#testimonials">ESTADIA E POUSADAS</a>
              </li>
              <li class="relative text-white after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[2px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">
                <a href="#testimonials">VOOS</a>
              </li>
            </ul>
          </div>
      </div>
    </div>
    </div>

  </section>
<main class="absolute h-dvh w-full top-0 left-0 bg-[url('/fundo.jpg')] bg-cover">
  <div class=""><img src="../public/Switzerland Travel New.png" height="1368" width="1936"/>
    <h1 class="absolute top-96 left-1/4 text-4xl shadow-gray-900">Venha conhecer o pais mais bonito do mundo</h1>
    <div>
    </div>
  </div>
</main>
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
