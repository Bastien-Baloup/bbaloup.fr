<script setup>
import { ref } from 'vue'
import { NA, NButton, NIcon, NDrawer, NDrawerContent, NText } from 'naive-ui'
import { Menu } from '@vicons/ionicons5'

const mobileMenuIsOpen = ref(false)
const openMobileMenu = () => mobileMenuIsOpen.value = true
const closeMobileMenu = () => mobileMenuIsOpen.value = false

</script>

<template>
  <header
    class="fixed top-0 left-0 z-10 w-full box-border min-h-[4rem] h-[10vh] flex backdrop-blur-[2px] backdrop-grayscale-[50%] bg-[#46464755] shadow-md md:h-[7.5vh]">
    <n-a href="#home" class="flex-shrink-0 my-4 ml-5 mr-auto md:my-2 md:ml-[10vw] xl:ml-[15vw] flex items-center">
      <img src="icon.svg" alt="back to the top" class="h-full" />
      <n-text type="primary" class="leckerli hidden xl:block text-[2rem] 2xl:text-[3rem] ml-4"><span class="lily">B</span>astien <span class="lily">B</span>aloup</n-text>
    </n-a>
    <nav class="hidden justify-end sm:flex my-auto mr-0 text-[1.25rem] underline-offset-2 md:mr-[10vw] md:text-[1.4rem] md:underline-offset-1 xl:mr-[15vw] 2xl:underline-offset-2 2xl:text-[2rem]">
      <n-a href="#home">Accueil</n-a>
      <n-a href="#skills">Mes&nbsp;Compétences</n-a>
      <n-a href="#projects">Mes&nbsp;Projets</n-a>
      <n-a href="#contact">Contact</n-a>
    </nav>
    <n-button circle class=" my-auto mr-5 sm:hidden" @click="openMobileMenu">
      <template #icon>
        <n-icon><Menu/></n-icon>
      </template>
    </n-button>
    <n-drawer v-model:show="mobileMenuIsOpen" class="bg-[#464647EE] backdrop-blur-[2px] backdrop-grayscale-[50%] shadow-md">
      <n-drawer-content title="Menu" closable :auto-focus="false">
        <nav class="flex flex-col justify-end my-auto mr-0 text-[1.25rem] underline-offset-2">
          <n-a href="#home" @click="closeMobileMenu">Accueil</n-a>
          <n-a href="#skills" @click="closeMobileMenu">Mes&nbsp;Compétences</n-a>
          <n-a href="#projects" @click="closeMobileMenu">Mes&nbsp;Projets</n-a>
          <n-a href="#contact" @click="closeMobileMenu">Contact</n-a>
        </nav>
      </n-drawer-content>
    </n-drawer>
  </header>
</template>

<style scoped lang="postcss">
nav .n-a {
  @apply mx-2 text-white 2xl:mx-4 hover:underline focus:underline focus:outline-none
}
</style>