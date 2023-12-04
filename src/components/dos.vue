<script setup>
import { ref, onMounted } from 'vue';

const IEL = ref('');
const IEF = ref('');
const IIL = ref('');
const IIF = ref('');
const IEML = ref('');
const IEMF = ref('');
const ISCL = ref('');
const ISCF = ref('');
const IERL = ref('');
const IERF = ref('');

onMounted(async () => {
  try {
    const response = await fetch('https://sitmotul.com.mx/api/statusEvalIng');
    const data = await response.json();

    // Sección IE
    IEL.value = `Al día de hoy se han realizado ${data['IE']['listas']} evaluaciones`;
    IEF.value = `Faltan por realizarse ${data['IE']['faltantes']} evaluaciones`;

    // Sección II
    IIL.value = `Al día de hoy se han realizado ${data['II']['listas']} evaluaciones`;
    IIF.value = `Faltan por realizarse ${data['II']['faltantes']} evaluaciones`;

    // Sección IEM
    IEML.value = `Al día de hoy se han realizado ${data['IEM']['listas']} evaluaciones`;
    IEMF.value = `Faltan por realizarse ${data['IEM']['faltantes']} evaluaciones`;

    // Sección ISC
    ISCL.value = `Al día de hoy se han realizado ${data['ISC']['listas']} evaluaciones`;
    ISCF.value = `Faltan por realizarse ${data['ISC']['faltantes']} evaluaciones`;

    // Sección IER
    IERL.value = `Al día de hoy se han realizado ${data['IER']['listas']} evaluaciones`;
    IERF.value = `Faltan por realizarse ${data['IER']['faltantes']} evaluaciones`;

  } catch (error) {
    console.error('Error al obtener datos:', error);
  }
});
</script>


<template>
  <body class="bg-sky-600">

  <div class="flex flex-row gap-x-5">

<!-- Primer bloque -->
<div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 flex flex-row gap-x-5 px-0 fonddown bg-yellow-400 mb-8">
  <div class="flex flex-col w-full gap-y-5 fond">
    <!-- IE -->
    <div class="w-full flex flex-col gap-y-3 border-2 rounded border-black px-3 py-1 shadow-lg">
      <h1 class="text-center text-2xl font-bold">Ingeniería Industrial</h1>
      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IIL">{{ IIL }}</h2>
      </div>

      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IIF">{{ IIF }}</h2>
      </div>
    </div>
  </div>
</div>

<!-- Segundo bloque -->
<div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 flex flex-row gap-x-5 px-0 fonddown bg-yellow-400 mb-8">
  <div class="flex flex-col w-full gap-y-5 fond">
    <!-- IE -->
    <div class="w-full flex flex-col gap-y-3 border-2 rounded border-black px-3 py-1 shadow-lg">
      <h1 class="text-center text-2xl font-bold">Ingeniería Renovables</h1>
      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IERL">{{ IERL }}</h2>
      </div>

      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IERF">{{ IERF }}</h2>
      </div>
    </div>
  </div>
</div>

<div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 flex flex-row gap-x-5 px-0 fonddown bg-yellow-400 mb-8">
  <div class="flex flex-col w-full gap-y-5 fond">
    <!-- IE -->
    <div class="w-full flex flex-col gap-y-3 border-2 rounded border-black px-3 py-1 shadow-lg">
      <h1 class="text-center text-2xl font-bold">Ingeniería Sistemas </h1>
      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="ISCL">{{ ISCL }}</h2>
      </div>

      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="ISCF">{{ ISCF }}</h2>
      </div>
    </div>
  </div>
</div>
<div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 flex flex-row gap-x-5 px-0 fonddown bg-yellow-400 mb-8">
  <div class="flex flex-col w-full gap-y-5 fond">
    <!-- IE -->
    <div class="w-full flex flex-col gap-y-3 border-2 rounded border-black px-3 py-1 shadow-lg">
      <h1 class="text-center text-2xl font-bold">Ingeniería Electronica </h1>
      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IEL">{{ IEL }}</h2>
      </div>

      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IEF">{{ IEF }}</h2>
      </div>
    </div>
  </div>
</div>

<!-- Segundo bloque -->
<div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 flex flex-row gap-x-5 px-0 fonddown bg-yellow-400 mb-8">
  <div class="flex flex-col w-full gap-y-5 fond">
    <!-- IE -->
    <div class="w-full flex flex-col gap-y-3 border-2 rounded border-black px-3 py-1 shadow-lg">
      <h1 class="text-center text-2xl font-bold">Ingeniería </h1>
      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IEML">{{ IEML }}</h2>
      </div>

      <div class="w-full flex flex-row gap-x-1 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-12 h-12">
          <!-- SVG Path para el ícono -->
        </svg>
        <h2 id="IEMF">{{ IEMF }}</h2>
      </div>
    </div>
  </div>
</div>
  </div>

  </body>
  </template>
  
 
  
  <style scoped>
  /* Agrega estilos según sea necesario */
  </style>
  