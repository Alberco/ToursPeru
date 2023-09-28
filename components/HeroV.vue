<template>
  <section class="
            relative 
            h-screen w-full mx-auto 
            px-2 md:px-4 lg:px-5
            py-2 md:py-4 lg:py-5">
    <picture class="">
      <img src="/back3.jpg" 
           class="
            h-full w-full 
            object-cover 
            rounded-md"  
            alt="logo" />
    </picture>
    <div class="
          absolute 
          top-4 bottom-4 
          inset-x-4 md:inset-x-10 lg:inset-x-20  
          grid grid-cols-1 lg:grid-cols-2 grid-flow-row">
      <!-- #seccion1 -->
      <article 
          class="
          flex flex-col items-center justify-center lg:justify-end  
          px-4 md:px-0">
        <p class="
          text-4xl md:text-6xl lg:text-7xl 
          text-white 
          font-bold 
          mb-6">
          Descubre la Magia de Perú con Nosotros
        </p>
        <p class="
          text-base md:text-2xl 
          text-white font-medium 
          leading-snug md:leading-normal">En Perú Explora Tours , te ofrecemos la puerta de entrada a la riqueza cultural y la diversidad natural de Perú. Como expertos en viajes, hemos forjado sólidos convenios con museos, restaurantes de renombre y otros destinos destacados en todo el país. Esto nos permite crear experiencias únicas y completas que te sumergen en la auténtica Perú.</p>
      </article>
       <!-- #seccion2 -->
      <article class="
              col-span-2 
              flex justify-start items-center 
              h-full ">
        <form class="
                    flex flex-wrap justify-center items-center 
                    gap-3 md:gap-4 lg:gap-8">
          <div class="
                  bg-white 
                  px-2 py-2 md:px-3 md:py-3 lg:px-4 lg:py-5 
                  rounded-md 
                  flex gap-2 items-center">
            <label for="locacion" class="font-bold">Locación: </label>
            <select id="locacion" name="locacion" class="py-1 w-40 text-black/60" >
              <option value="manzana">Lima</option>
              <option value="banana">Arequipa</option>
              <option value="uva">Puno</option>
              <option value="fresa">Trujillo</option>
              <option value="naranja">Selva</option>
            </select>
          </div> 
          <div class="
                  bg-white 
                    px-2 py-2 md:px-3 md:py-3 lg:px-4 lg:py-5 
                    rounded-md 
                    flex gap-2 items-center">
            <label for="personas" class="font-bold">Personas: </label>
              <select id="personas" name="personas" class="py-1 w-40 text-black/60" >
                <option value="manzana">1</option>
                <option value="banana">2</option>
                <option value="uva">3</option>
                <option value="fresa">4</option>
                <option value="naranja">5</option>
              </select>
          </div> 
          <div class="
                    bg-white 
                    px-2 py-3 md:px-3 md:py-3 lg:px-4 lg:py-5 
                    rounded-md 
                    flex gap-2 items-center">
            <label for="price" class="font-bold">Precio total: </label>
            <input type="range" id="price" name="price" min="0" max="100" value="50" class="py-1 w-40 text-black/60 accent-orange-500">
          </div>
          <div class="flex items-center justify-center">
            <button class=" 
                          w-40 
                          px-4 py-4 
                          rounded-md 
                          bg-orange-500 
                          text-white 
                          font-bold">Buscar Paquetes</button>
          </div>
        </form>
      </article>
    </div>
  </section>
</template>