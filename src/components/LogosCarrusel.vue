<script setup>
import Html5 from '../assets/html5.svg';
import CSS from '../assets/css.svg';
import Bootstrap from '../assets/bootstrap.svg';
import JavaScript from '../assets/javascript.svg'
import Git from '../assets/git.svg'
import GitHub from '../assets/github.svg'
import Vue from '../assets/vuedotjs.svg'
import TailwindCss from '../assets/tailwindcss.svg'
import Figma from '../assets/figma.svg'
import AfterEffects from '../assets/adobe-after-effects.svg'

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