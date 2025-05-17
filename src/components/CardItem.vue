<template>
  <div class="bg-base-100 shadow-sm text-white p-2 border-2 border-gray-700/50 rounded-lg md:w-auto md:flex md:items-center gap-15">
    <figure class="rounded-t-lg">
      <img
        class="rounded-tl-lg rounded-br-lg aspect-auto md:w-90 md:h-80 md:rounded-lg "
        :src="proyectos.imagen"
        alt="Album"
      />
    </figure>
    <div class="card-body pt-5">
      <h2 class="text-2xl font-bold">{{ proyectos.nombre }}</h2>
      <p class="text-gray-300 pt-2">{{ proyectos.descripcion }}</p>
      <ul class="flex flex-row gap-3 py-5">
        <li v-for="(tecnologia, index) in proyectos.tecnologias" :key="index">
          <img
            :src="tecnologia.icono"
            :alt="'Icono de ' + tecnologia.nombre"
            class="w-6 h-6 filter brightness-0 invert"
          />
        </li>
      </ul>
      <div class="justify-end">
        <a :href="proyectos.url" target="_blank" rel="noopener noreferrer">
          <button class="bg-violet-500 px-8 py-3 rounded-sm hover:bg-violet-800">Listen</button>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardItem",
  props: {
    proyectos: Object,
  },
  setup() {},
};
</script>