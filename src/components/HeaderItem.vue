<template>
    <header
    class="bg-gray-800 mt-5 mx-auto min-h-90 max-w-6xl text-white max-sm:w-1xl"
    id="home"
  >
    <div
      class="pl-3 pt-30 block md:pl-10 md:flex md:items-center md:justify-center md:pt-10"
    >
      <div class="">
        <p class="text-base lg:text-2xl">Hola, bienvenido.</p>
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
        <p class="text-base lg:text-2xl">puedo ayudarte a diseñar tu página web</p>
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
</template>
<script setup>
</script>

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