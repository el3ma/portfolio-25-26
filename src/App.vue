<script setup>
import Navbar from "./components/NavbarItem.vue";
import LogoCarrusel from "./components/LogosCarrusel.vue";
import Proyectos from "./components/Proyectos.vue";
import FooterItem from "./components/FooterItem.vue";
</script>

<template>
  <!-- Navbar -->
  <div class="relative">
    <Navbar class="fixed -top-1 right-0 left-0 z-10" />
  </div>
  <!-- Header -->
  <header
    class="bg-gray-800 mt-10 mx-auto min-h-90 max-w-6xl text-white max-sm:w-1xl"
    id="home"
  >
    <div
      class="p-5 pt-15 block md:pl-10 md:flex md:items-center md:justify-center"
    >
      <div class="">
        <p class="text-2xl sm:text-4xl">Hola, bienvenido.</p>
        <div class="wrapper md:pb-5">
          <h1 class="text-4xl font-bold pb-2 md:text-7xl">Soy</h1>
          <div class="words">
            <span class="header__name text-4xl font-bold md:text-7xl"
              >Emanuel Astudillo</span
            >
            <span class="header__name text-4xl font-bold md:text-7xl"
              >Front-End Developer</span
            >
            <span class="header__name text-4xl font-bold md:text-7xl"
              >Diseñador UX/UI</span
            >
            <span class="header__name text-4xl font-bold md:text-7xl"
              >Emanuel Astudillo</span
            >
          </div>
        </div>
        <p class="text-2xl">puedo ayudarte a diseñar tu página web</p>
      </div>
      <div class="header__logo">
        <img
          class="max-md:hidden md:size-120"
          src="/public/imgs/logo_Ema_grande.svg"
          alt="logo"
        />
      </div>
    </div>
  </header>
  <!-- Sobre mí -->
  <section
    class="text-white bg-gray-800 mt-10 mx-5 md:mx-auto md:max-w-5xl min-h-90 md:flex md:items-center md:justify-center gap-10"
    id="sobreMi"
  >
    <!--  <div class="grid place-content-center pb-10"> -->
    <img class="aspect-auto w-90 rounded-l-lg mask-t-from-90% mask-b-from-60%" src="/public/imgs/IMG_8101.png" alt="" />
    <!-- </div> -->
    <article class="max-w-3xl">
      <h2 class="text-3xl font-medium py-5">Sobre mí</h2>
      <p>
        Hola, soy Emanuel Astudillo. Residente en Villa Alemana, Chile, mi
        trayectoria profesional se inició en el ámbito audiovisual,
        desarrollando una sólida comprensión de la <span class="font-bold">narrativa visual</span> a través de
        la edición de video freelance. Buscando expandir mi impacto en la
        creación de experiencias, di un giro hacia el <span class="font-bold">Diseño de Experiencia de
        Usuario (UX/UI)</span> con un intensivo Bootcamp en 2021. Esta formación fue
        fundamental para adquirir habilidades clave en <span class="font-bold">investigación, diseño
        centrado en personas y prototipado</span>, al tiempo que potenció mi capacidad
        para el <span class="font-bold">trabajo en equipo</span> y el <span class="font-bold">liderazgo</span>. Esta experiencia me llevó a
        colaborar activamente como ayudante de profesor en UX/UI. Actualmente,
        aplico esta perspectiva única que combina la visión audiovisual con el
        diseño estratégico centrado en el usuario para crear <span class="font-bold">soluciones
        digitales funcionales y atractivas</span> en mis proyectos. Te invito a
        explorar mi portafolio para conocer mi trabajo.
      </p>
      <font-awesome-icon icon="fa-solid fa-house" />
    </article>
  </section>
  <section id="skills" class="py-30 mx-10">
    <div class="max-w-5xl mx-auto">
      <h3 class="text-3xl font-medium text-white">Skills</h3>
    </div>
    <LogoCarrusel class="py-5" />
  </section>
  <section class="" id="proyectos">
    <Proyectos />
  </section>
  <FooterItem />
</template>

<style scoped>
.wrapper {
  gap: 5px;
  width: 100%;
  height: 90px;
  box-sizing: content-box;
}

.header__name {
  background: linear-gradient(135deg, #9d4de2 6.66%, #568ada 85.61%);
  background-clip: text;
  color: transparent;
  display: block;
  padding-bottom: 8px;
}

.words {
  overflow: hidden;
  height: 40px;
}

.wrapper span {
  animation: spin_words 6s infinite;
}

@keyframes spin_words {
  10% {
    transform: translateY(-110%);
  }

  25% {
    transform: translateY(-100%);
  }

  35% {
    transform: translateY(-100%);
  }

  50% {
    transform: translateY(-212%);
  }

  60% {
    transform: translateY(-200%);
  }

  75% {
    transform: translateY(-200%);
  }

  85% {
    transform: translateY(-312%);
  }

  100% {
    transform: translateY(-300%);
  }
}

.header__text {
  font-size: 2.5rem;
}

@media (min-width: 720px) {
  .wrapper {
    display: flex;
    width: 850px;
    height: 75px;
  }
  .words {
    height: 100%;
  }
}
</style>
