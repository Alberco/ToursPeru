
import { NuxtLink } from '#build/components';
<template>
  <nav class="backdrop-blur-md bg-black/80 mx-2 md:mx-4 mt-4 rounded-md z-50 ">
    <div class="py-2 flex justify-between items-center px-2 md:px-16">
      <ul class="text-xs md:text-xl">
        <li class="flex flex-col font-bold text-white ">Perú <span class=" font-bold">Explora Tours</span></li>
      </ul>
      <ul class="flex items-center gap-4 md:gap-10 text-sm md:text-base font-medium  tracking-wide text-white ">
        <li>
          <NuxtLink to="/">
            Inicio
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/catalogo">
            Tours
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/contact">
            Contact
          </NuxtLink>
        </li>
        <li class="px-2 md:px-6 py-2 rounded-md text-white bg-orange-500 text-xs md:text-base">
          <button class="">Sign up</button>
        </li>
      </ul>
    </div>
  </nav>
</template>