<script setup lang="ts">

interface UserFeedback {
  id: number
  name: string
  img: string
  description: string
}

import { reactive } from "vue"

const testimonioUser = reactive([
  {id: 2948 , name : "Noah Nilse", description:"Los museos en Perú son fascinantes. Aprendí mucho sobre la rica historia del país. Definitivamente, un destino culturalmente enriquecedor" , img: "/user2.jpg"},
  {id:23176 , description: " Mi viaje a Perú fue inolvidable. Los tours, los festivales y los restaurantes fueron simplemente espectaculares. ¡Gracias por una experiencia increíble!" , img: "/user1.jpg",name: "Herminia Byrd"  },
  {id: 76612, description: "Los eventos en Perú son una explosión de diversión. Disfruté mucho de los festivales y la comida deliciosa. ¡Volveré pronto!" , img: "/user3.jpg",name: "Tonya Hart"  },
])
</script>


<template>
  <section class="
                  grid grid-cols-1  
                  lg:grid-cols-2 
                  h-full 2xl:h-screen w-full">
    <article class="w-full h-full relative">
      <p class="
                absolute inset-0 
                text-xl md:text-4xl lg:text-5xl  xl:text-7xl 
                flex flex-col justify-center items-center  
                text-white font-medium" >
        <span class="text-xl text-gray-200">Testimonios</span>
        Nuestros clientes opinan
      </p>
      <video width="340" height="240" class="w-full h-full object-cover" autoplay muted loop >
        <source src="/servicio.mp4" type="video/mp4" >
      </video>
    </article>
    <article class="
              py-2 md:py-6 
              grid grid-cols-1 grid-rows-3 place-items-center 
              gap-4 
              w-full h-full">
      <section v-for="(feedback, index) in testimonioUser" :key="feedback.id" 
                  class=" 
                  w-[70%] h-[80%] 
                  px-6 py-4 
                  grid gap-0 md:gap-2 grid-flow-col grid-rows-4  md:grid-rows-3
                  rounded-xl shadow-2xl ">
        <img src="/comillas.png" width="40" height="40" alt="logo comill" class="col-span-2 self-start ">
        <p class="col-span-2 ">{{ feedback.description  }}</p>
        <p class=" col-span-2 flex gap-2 items-center font-medium text-lg">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-user-circle-2"><path d="M18 20a6 6 0 0 0-12 0"/><circle cx="12" cy="10" r="4"/><circle cx="12" cy="12" r="10"/></svg> 
          {{ feedback.name  }}</p>
        <div class=" row-span-1  md:row-span-3 place-self-center ">
          <img :src="feedback.img" width="100" height="100" :alt="feedback.name" class="rounded-full" >
        </div>
      </section>
    </article>
  </section>
</template>