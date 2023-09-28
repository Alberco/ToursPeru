<script setup lang="ts">

interface ListImagenDinamica {
  id: number
  path: string
  name: string
}

import { ref,reactive } from "vue"
import type { Ref } from 'vue'

const imagenDinamica: Ref<string> = ref("/back6.jpg")

const updateImgDinamica = (url:string) => {
  imagenDinamica.value = url;
} 

const listaImg: Array<ListImagenDinamica> = reactive([
  { "id": 23411, "path": "/back6.jpg", "name": "cuscoImg" },
  { "id": 2341311, "path": "/back.jpg", "name": "cuscoImg" },
  { "id": 234221311, "path": "/back2.jpg", "name": "cuscoImg" },
])

</script>

<template>
  <section class="
                  grid grid-cols-1 lg:grid-cols-2 grid-flow-row-dense lg:grid-rows-1 justify-items-center
                  h-full xl:h-screen">


    <article class="
                  relative 
                  px-2 md:px-4 lg:px-5
                  py-2 md:py-4 lg:py-5
                  h-full
                  ">
      <picture>
        <img alt="servicio1" :src="imagenDinamica" class="h-full w-full rounded-xl lg:rounded-tl-xl lg:rounded-bl-xl lg:rounded-tr-none lg:rounded-br-none object-cover " />
      </picture>
      <p class=" 
                absolute 
                bottom-12 inset-x-8 
                text-4xl 
                text-white 
                font-semibold 
                flex gap-1">
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-white "><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>
        </span> 
         Perú - Cusco</p>
    </article>
    <article class="
                  grid grid-rows-6  w-full h-full
                  py-4 content-center">
      <div class="pl-4 row-span-2 lg:row-span-4 h-full">
        <p class="
                  text-4xl md:text-6xl lg:text-7xl xl:text-8xl 
                  w-full 
                  pr-8 
                  font-medium">Descubre Cusco,</p>
        <p class="
                  text-4xl md:text-6xl lg:text-7xl xl:text-8xl 
                  w-full 
                  pr-8 
                  font-medium">aventura inolvidable.</p>
        <ul class="
                  flex flex-wrap 
                  gap-3 
                  mt-4 ">
            <li class="rounded-xl px-4 py-1 text-sm border-orange-500 border-2 text-black font-medium">Aguas termales</li>
            <li class="rounded-xl px-4 py-1 text-sm border-orange-500 border-2 text-black font-medium">Aventura</li>
            <li class="rounded-xl px-4 py-1 text-sm border-orange-500 border-2 text-black font-medium">Gastronomia</li>
            <li class="rounded-xl px-4 py-1 text-sm border-orange-500 border-2 text-black font-medium">Valles</li>
            <li class="rounded-xl px-4 py-1 text-sm border-orange-500 border-2 text-black font-medium">Festivales</li>
        </ul>
      </div>
      <div class="
                  row-span-4
                  lg:row-span-2 
                  w-full h-full 
                  pl-4  
                  flex flex-col justify-end ">
          <ul class="
                    flex justify-start flex-wrap gap-5">
              <li v-for="(imagen) in listaImg" key="imagen.id" class="w-20 md:w-28 lg:w-40 h-full">
                <button @click="updateImgDinamica(imagen.path)" class="w-full h-full">
                  <img :src="imagen.path" :alt="imagen.name" class="w-full object-cover rounded-md " >
                </button>
              </li>
          </ul>
          <p class=" 
                    text-sm md:text-basic lg:text-lg text-black/60 
                    pr-4 pt-2 
                    overflow-y-scroll
                    ">
          Cusco, situado en el corazón de los Andes peruanos, es una ciudad histórica y fascinante que combina la riqueza de su herencia incaica con la belleza de su arquitectura colonial y la puerta de entrada a la majestuosidad de Machu Picchu. Únete a nosotros en un viaje lleno de cultura, historia y maravillas naturales. Experimenta la hospitalidad peruana a través de nuestros socios de restaurantes, y sumérgete en el arte y la historia en nuestros museos asociados.</p>
      </div>
    </article>


  </section>
</template>