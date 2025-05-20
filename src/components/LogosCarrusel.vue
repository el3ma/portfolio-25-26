<script setup>
import Html5 from '/public/imgs/tecnologias/html5.svg';
import CSS from '/public/imgs/tecnologias/css.svg';
import Bootstrap from '/public/imgs/tecnologias/bootstrap.svg';
import JavaScript from '/public/imgs/tecnologias/javascript.svg'
import Git from '/public/imgs/tecnologias/git.svg'
import GitHub from '/public/imgs/tecnologias/github.svg'
import Vue from '/public/imgs/tecnologias/vuedotjs.svg'
import TailwindCss from '/public/imgs/tecnologias/tailwindcss.svg'
import Figma from '/public/imgs/tecnologias/figma.svg'
import AfterEffects from '/public/imgs/tecnologias/adobe-after-effects.svg'

const logos = [
  { src: Html5, alt: 'HTML5' },
  { src: CSS, alt: 'CSS' },
  { src: Bootstrap, alt: 'Bootstrap' },
  { src: JavaScript, alt: 'JavaScript'},
  { src: Git, alt: 'Git'},
  { src: GitHub, alt: 'Github'},
  { src: Vue, alt: 'Vue'}, 
  { src: TailwindCss, alt: 'TailwindCss'},
  { src: Figma, alt: 'Figma'},
  { src: AfterEffects, alt: 'After Effects'}
];
</script>

<template>
    <div class="w-full inline-flex flex-nowrap overflow-hidden [mask-image:_linear-gradient(to_right,transparent_0,_black_50px,_black_calc(100%-50px),transparent_100%)]">
      <!-- Primer conjunto -->
      <ul class="flex items-center [&_img]:max-w-none animate-infinite-scroll">
        <li v-for="logo in logos" :key="logo.alt" class="mx-8">
          <img :src="logo.src" :alt="logo.alt" class="h-12 filter brightness-0 invert" />
        </li>
      </ul>
      <!-- Segundo conjunto (duplicado) -->
      <ul class="flex items-center [&_img]:max-w-none animate-infinite-scroll" aria-hidden="true">
        <li v-for="logo in logos" :key="`copy-${logo.alt}`" class="mx-8">
          <img :src="logo.src" :alt="logo.alt" class="h-12 filter brightness-0 invert" />
        </li>
      </ul>
    </div>
  </template>

<style>
@keyframes infinite-scroll {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
.animate-infinite-scroll {
  animation: infinite-scroll 20s linear infinite;
}
</style>