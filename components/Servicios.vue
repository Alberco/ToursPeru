<script setup lang="ts">
interface ImageEvent {
  id: number
  path: string
  name: string
  description: string
}

import { ref, reactive } from "vue"
import type { Ref } from 'vue'

const eventos : Array<ImageEvent> = reactive([
  {id : 113223, path: "/event1.jpg", name:"Restaurantes" , description: " La gastronomía peruana es famosa en todo el mundo por su diversidad y sabor. Los restaurantes en Perú ofrecen una deliciosa mezcla de influencias indígenas, europeas, asiáticas y africanas."},
  {id : 12133223, path: "/event2.jpg", name:"Museos" , description: "Perú alberga una riqueza de museos que ofrecen una visión fascinante de su historia y cultura. El Museo Larco en Lima exhibe una impresionante colección de arte precolombino, mientras que el Museo de la Nación ofrece una visión completa de la historia peruana."},
  {id : 12131213223, path: "/event3.jpg", name:"Eventos" , description: "Perú alberga una amplia gama de eventos culturales, deportivos y artísticos durante todo el año. Esto incluye festivales folclóricos, desfiles, competencias deportivas como el Rally Dakar y eventos de música y danza tradicionales."},
  {id : 213, path: "/event4.jpg", name:"Expediciones" , description: "Los festivales en Perú son una parte importante de la vida cultural del país. Desde el famoso Inti Raymi en Cusco, que celebra el solsticio de invierno, hasta el Carnaval de Cajamarca y la Fiesta de la Virgen de la Candelaria en Puno."}
])  


</script>

<template>
  <section class="
                  h-full w-full 
                  px-4 py-4">
<!--   <p class="text-5xl font-semibold">Eventos, Museos, Festivales y mucho mas. </p> -->
    <section class="
                  px-8 lg:px-16 py-4  lg:py-6 
                  w-full h-full 
                  rounded-lg 
                  grid grid-cols-1 grid-flow-row  md:grid-cols-4 place-items-center  gap-4 ">
      <p class="
                col-span-1 md:col-span-4  place-self-start
                text-4xl  
                pb-4 lg:pb-8 ">Descubre la Experiencia Total: Tours, Eventos, Restaurantes, Festivales y Museos</p>

      <article v-for="(evento, index) in eventos" :key="evento.id" class="group/info w-full h-full relative">
        <img :src="evento.path" :alt="evento.name" class="object-cover h-full w-full rounded-md" >
        <div class=" absolute bottom-0 text-transparent  inset-0 group-hover/info:bg-orange-500/90  group-hover/info:text-white  transition duration-200 flex flex-col items-center justify-center rounded-md ">
          <p class="text-xl font-semibold pb-1 ">{{ evento.name  }}</p>
          <p class="text-xs md:text-base px-4">{{  evento.description  }}</p>
        </div>
      </article>
    </section>
  </section>
</template>