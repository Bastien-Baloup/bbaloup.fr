<script setup>
import { NConfigProvider } from 'naive-ui'
import themeOverrides from './assets/naive-ui-Dracula-theme-overrides.json'
import Home from './components/Home.vue'
import Header from './components/Header.vue'
console.log(themeOverrides)
</script>

<template>
  <NConfigProvider :theme-overrides="themeOverrides">
    <Header />
    <Home />
  </NConfigProvider>
</template>

<style lang="postcss">
@import url('https://fonts.googleapis.com/css2?family=Lily+Script+One&family=Leckerli+One&display=swap');

@tailwind base;
@tailwind components;
@tailwind utilities;


body {
  --shiftX: 0;
  --shiftY: 0;
  background-color: #464647;
  overflow-x: hidden;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.lily {
  font-family: 'Lily Script One', cursive;
}
.leckerli {
  font-family: 'Leckerli One', cursive;
}
</style>
