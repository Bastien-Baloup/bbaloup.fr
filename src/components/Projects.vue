<script setup>
import { NH2, NH3, NGrid, NGridItem, NThing, NTag, NP } from 'naive-ui';
</script>

<template>
  <section id="projects" class="scroll-mt-[15vh] min-h-screen h-max">
    <n-h2 
      prefix="bar" align-text
      class="text-[1.25rem] ml-5 mb-[4rem] md:text-[1.75rem] 2xl:text-[2rem] 2xl:ml-6">
      Mes Projets
    </n-h2>
    <n-grid cols="1 l:2 2xl:3" x-gap="0 l:16 xl:32 2xl:64" y-gap="16 xl:32 2xl:64" responsive="screen" class="h-max">
      <n-grid-item>
        <n-thing>
          <template #avatar>
            <img src="http://via.placeholder.com/1980x1080" alt="" class="">
          </template>
          <template #header>
            <n-h3 class="w-max">
              Project name
            </n-h3>
          </template>
          <template #description>
            <div class="tag-list">
              <n-tag type="info">Full Stack</n-tag>
              <n-tag type="success">Vue.js</n-tag>
              <n-tag type="success">Node.Js</n-tag>
            </div>
          </template>
          <n-p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Maxime eveniet corporis dolorem laboriosam, amet non dicta, assumenda, sequi placeat iste velit minus rem accusantium!
          </n-p>
        </n-thing>
      </n-grid-item>
      <n-grid-item>
        <n-thing>
          <template #avatar>
            <img src="http://via.placeholder.com/1980x1080" alt="" class="">
          </template>
          <template #header>
            <n-h3 class="w-max">
              Project name
            </n-h3>
          </template>
          <template #description>
            <div class="tag-list">
              <n-tag type="info">Full Stack</n-tag>
              <n-tag type="success">Vue.js</n-tag>
              <n-tag type="success">Node.Js</n-tag>
            </div>
          </template>
          <n-p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Recusandae dolorum molestiae mollitia deleniti, fugiat repudiandae quibusdam, Doloremque.
          </n-p>
        </n-thing>
      </n-grid-item>
      <n-grid-item>
        <n-thing>
          <template #avatar>
            <img src="http://via.placeholder.com/1980x1080" alt="" class="">
          </template>
          <template #header>
            <n-h3 class="w-max">
              Project name
            </n-h3>
          </template>
          <template #description>
            <div class="tag-list">
              <n-tag type="info">Full Stack</n-tag>
              <n-tag type="success">Vue.js</n-tag>
              <n-tag type="success">Node.Js</n-tag>
            </div>
          </template>
          <n-p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Voluptatibus atque laboriosam vel corporis debitis dignissimos molestias consequatur quo?
          </n-p>
        </n-thing>
      </n-grid-item>
      <n-grid-item>
        <n-thing>
          <template #avatar>
            <img src="http://via.placeholder.com/1980x1080" alt="" class="">
          </template>
          <template #header>
            <n-h3 class="w-max">
              Project name
            </n-h3>
          </template>
          <template #description>
            <div class="tag-list">
              <n-tag type="info">Full Stack</n-tag>
              <n-tag type="success">Vue.js</n-tag>
              <n-tag type="success">Node.Js</n-tag>
            </div>
          </template>
          <n-p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit.
            Tempore harum eos laborum quo minima reprehenderit saepe inventore laudantium, fugiat sequi.
          </n-p>
        </n-thing>
      </n-grid-item>
    </n-grid>
  </section>
</template>

<style scoped lang="postcss">
img {
 @apply relative top-1/2 -translate-y-1/2; 
}
.n-h3 {
  @apply mb-1;
}
.tag-list {
  @apply flex flex-wrap md:flex-nowrap;
}
.n-tag {
  @apply m-1;
}
.n-tag__content {
 @apply text-sm lg:text-base xl:text-xl;  
}
.n-thing {
  @apply bg-gray-600/90 border rounded-md border-purple p-6 h-full;
}

.n-p {
  @apply text-base lg:text-lg xl:text-xl;
}
</style>