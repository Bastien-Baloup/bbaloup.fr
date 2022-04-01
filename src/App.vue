<script setup>
import Background from './components/Background.vue'
</script>

<template>
  <Background />
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
}
</style>
