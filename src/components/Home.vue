<script setup>
import Background from './Background.vue'
import { NH1, NH2, NText, NP } from 'naive-ui'
</script>

<template>
  <Background class="max-h-[90vh]"/>
  <section class="ml-[5vw] mt-[15vh] md:ml-[10vw] md:mt-[20vh] max-h-[90vh] mb-[400vh]">
    <NH1 type="primary" class="leckerli text-[2.5rem] md:text-[4rem] 2xl:text-[6rem]">
      <NText type="primary" class="leckerli"><span class="lily">B</span>astien <span class="lily">B</span>aloup</NText>
    </NH1>
    <NH2 prefix="bar" align-text class="text-[1.25rem] ml-5 -mt-6 md:text-[1.75rem] md:-mt-8 2xl:text-[2rem] 2xl:ml-6 2xl:-mt-10">
      Developpeur Web Full-stack
    </NH2>
    <NP depth="2" class="mt-[20vh] mr-[5vw] max-w-[120ch] text-[1.25rem] md:mr-[10vw] md:text-[1.5rem]">
      Proffesionnel qualifié, aussi compétent en Front-end qu’en Back-end. Certifié méthodes Agiles et qualité web.<br>
      Fort de ma capacité d’adaptation, je travaille aussi bien en équipe ou en autonomie.<br>
      Attaché à rendre un travail soigné dans les temps impartis, je suis ouvert à vos propositions.
    </NP>
  </section>
</template>