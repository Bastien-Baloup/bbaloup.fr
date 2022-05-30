<script setup>
import Background from './Background.vue'
import { NH1, NH2, NText, NP } from 'naive-ui'
</script>

<template>
  <Background class="max-h-[90vh]" />
  <section id="home" class="ml-[10vw] mt-[15vh] md:ml-[15vw] xl:ml-[20vw] md:mt-[20vh] max-h-[90vh] mb-[15vh] scroll-mt-[15vh]">
    <n-h1 type="primary" class="leckerli text-[2.5rem] md:text-[4rem] 2xl:text-[6rem]">
      <n-text type="primary" class="leckerli"><span class="lily">B</span>astien <span class="lily">B</span>aloup</n-text>
    </n-h1>
    <n-h2
      prefix="bar" align-text
      class="text-[1.25rem] ml-5 -mt-6 md:text-[1.75rem] md:-mt-8 2xl:text-[2rem] 2xl:ml-6 2xl:-mt-10">
      Developpeur Web Full-stack
    </n-h2>
    <n-p depth="2" class="mt-[15vh] mr-[10vw] md:max-w-[80ch] text-[1.25rem] md:mt-[20vh] md:mr-[15vw] md:text-[1.5rem] xl:mr-[20vw]">
      Proffesionnel qualifié, aussi compétent en Front-end qu’en Back-end. <br>
      Certifié méthodes Agiles et qualité web.<br>
      Fort de ma capacité d’adaptation, je travaille aussi bien en équipe ou en autonomie.<br>
      Attaché à rendre un travail soigné dans les temps impartis, je suis ouvert à vos propositions.
    </n-p>
  </section>
</template>