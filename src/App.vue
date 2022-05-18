<script setup>
import Background from './components/Background.vue'
import { NConfigProvider } from 'naive-ui'
import themeOverrides from './assets/naive-ui-Dracula-theme-overrides.json'
import Home from './components/Home.vue'
console.log(themeOverrides)
</script>

<template>
  <NConfigProvider :theme-overrides="themeOverrides">
    <Home />
    <Background />
  </NConfigProvider>
</template>

<style lang="postcss">
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  --shiftX: 0;
  --shiftY: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  image-rendering: pixelated;
}
</style>
