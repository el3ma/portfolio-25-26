<script setup>
import Navbar from "./components/NavbarItem.vue";
import HeaderItem from "./components/HeaderItem.vue";
import AboutMe from "./components/AboutMe.vue";
import LogoCarrusel from "./components/LogosCarrusel.vue";
import Proyectos from "./components/Proyectos.vue";
import FooterItem from "./components/FooterItem.vue";
</script>

<template>
  <!-- Navbar -->
  <!-- <div class="relative">
    <Navbar class="fixed -top-1 right-0 left-0 z-10" />
  </div> -->
  <!-- Header -->
  <HeaderItem/>
  <!-- Sobre mí -->
  <AboutMe/>
  <section id="skills" class="py-30 md:mx-10">
    <div class="max-w-5xl mx-auto">
      <h3 class="text-3xl font-medium text-white max-sm:mx-10">Skills</h3>
    </div>
    <LogoCarrusel class="py-5" />
  </section>
  <section  id="proyectos">
    <Proyectos/>
  </section>
  <FooterItem />
</template>

<style scoped>

</style>
