<script setup>
import { NConfigProvider } from 'naive-ui'
import themeOverrides from './assets/naive-ui-Dracula-theme-overrides.json'
import Header from './components/Header.vue'
import Home from './components/Home.vue'
import Skills from './components/Skills.vue'
</script>

<template>
  <n-config-provider :theme-overrides="themeOverrides">
    <Header />
    <Home />
    <Skills />
  </n-config-provider>
</template>

<style lang="postcss">
@import url('https://fonts.googleapis.com/css2?family=Lily+Script+One&family=Leckerli+One&display=swap');

@tailwind base;
@tailwind components;
@tailwind utilities;

html {
  scroll-behavior: smooth;
}

body {
  --shiftX: 0;
  --shiftY: 0;
  background-color: #464647;
  overflow: overlay;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  @apply ml-[10vw] md:ml-[15vw] xl:ml-[20vw] max-w-[80vw] md:max-w-[70vw]  xl:max-w-[60vw]
}
*{
  scrollbar-color: #636372 transparent !important;
}
::-webkit-scrollbar {
  width: 0.4rem;
  z-index: 1;
}
::-webkit-scrollbar-track {
  @apply bg-transparent;
}
::-webkit-scrollbar-thumb {
  @apply bg-white z-50 rounded-full;
}

.lily {
  font-family: 'Lily Script One', cursive;
}
.leckerli {
  font-family: 'Leckerli One', cursive;
}
</style>
