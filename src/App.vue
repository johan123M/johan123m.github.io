<script setup>
import Cargar from './components/Cargar.vue';
import inge from './components/inge.vue';
import uno from './components/uno.vue';
import dos from './components/dos.vue';
</script>

<template>
  <header>
    <Cargar></Cargar>
  </header>

    <body>
    <inge></inge>

    <div class="espacio"></div>
      <dos></dos>
      
    <div class="espacio"></div>
    <uno></uno>

    <div class="espacio"></div>

   
  </body>


</template>

<style>
  /* Estilo para agregar espacio hacia abajo */
  .espacio {
     /* Ajusta el valor según tus necesidades */
    background-color: rgb(2,132,199); /* Cambia el color según tus preferencias */
    height: 40px; 
  }

 
</style>
