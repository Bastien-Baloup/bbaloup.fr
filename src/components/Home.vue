<script setup>
import Background from './Background.vue'
import { NH1, NH2, NText } from 'naive-ui'
</script>

<template>
  <Background class="max-h-[90vh]"/>
  <section class="w-screen max-h-[90vh] mb-[400vh]">
    <div class="ml-[5vw] mt-[15vh] md:ml-[10vw] md:mt-[20vh]">
      <NH1 class="text-[2.5rem] md:text-[4rem] 2xl:text-[6rem]">
        <NText type="primary" class="lily">B. Baloup</NText>
      </NH1>
      <NH2 prefix="bar" align-text class="text-[1.25rem] ml-5 -mt-6 md:text-[1.75rem] md:-mt-8 2xl:text-[2rem] 2xl:ml-6 2xl:-mt-10">
        <NText>Developpeur Web Full-stack</NText>
      </NH2>
    </div>
  </section>
</template>