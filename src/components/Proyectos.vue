<template>
   <div class="mx-auto max-w-5xl p-5 min-h-90 bg-gray-800 text-white">
      
      <CardItem v-for="itemProyecto in listaProyectos"
      :key="itemProyecto.id"
      :proyectos="itemProyecto"/>
   </div>
   </template>

<script>
import CardItem from './CardItem.vue'
export default {
   name: 'Proyectos',
   components: {
      CardItem
   },
   data() {
      return {
         listaProyectos: []
      }
   },
   async mounted() {
      try {
         let response = await fetch('/api/proyectos.json')
         let data = await response.json()
         console.log(data)
         this.listaProyectos = data
      } catch (error) {
         console.error('Error fetching proyectos:', error)
      }
   }
}
</script>