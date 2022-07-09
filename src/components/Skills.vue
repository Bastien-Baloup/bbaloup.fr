<script setup>
import { NH2, NList, NListItem, NThing, NH3, NH4, NP, NA } from 'naive-ui';
</script>

<template>
  <section id="skills" class="scroll-mt-[15vh] min-h-screen h-max">
    <n-h2 
      prefix="bar" align-text
      class="text-[1.25rem] ml-5 md:text-[1.75rem] 2xl:text-[2rem] 2xl:ml-6">
      Mes Compétences
    </n-h2>
    <div class="flex flex-col items-stretch min-h-[62rem] lg:min-h-[unset] lg:flex-row lg:h-max mt-8">
      <div class="card">
        <n-h3 align-text class="card-title">&nbsp;Languages et Frameworks&nbsp;</n-h3>
        <n-list class="mt-5 mb-auto">
          <n-list-item class="border-purple">
            <n-thing>
              <template #header>
                <n-h4>JavaScript</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  Vue.js&nbsp;/ React&nbsp;/<br>
                  Node.js&nbsp;/ Express
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing>
              <template #header>
                <n-h4>PHP</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  Symfony 4|5
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing>
              <template #header>
                <n-h4>CSS</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  SCSS&nbsp;/ Tailwind&nbsp;/<br>
                  Bootstrap
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing >
              <template #header>
                <n-h4>Autres Languages</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  HTML5&nbsp;/ Twig&nbsp;/ Python3&nbsp;/<br>
                  SQL&nbsp;/ JSON&nbsp;/ Markdown
                </n-p>
              </template>

            </n-thing>
          </n-list-item>
        </n-list>
      </div>
      <div class="card">
        <n-h3 align-text class="card-title">&nbsp;Compétences Transversales&nbsp;</n-h3>
        <n-list class="mt-5 mb-auto">
          <n-list-item class="border-purple">
            <n-thing>
              <template #header>
                <n-h4>Qualité Web</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  Certifié <n-a href="https://directory.opquast.com/fr/certificat/QJYKSD/" target="_blank" class="underline">OPQUAST</n-a>
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing>
              <template #header>
                <n-h4>Gestion de Projet</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  <n-a href="https://www.francecompetences.fr/recherche/rs/2085/" target="_blank" class="underline">Méthodes Agiles</n-a>&nbsp;/<br>
                  Scrum&nbsp;/ Kanban
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing>
              <template #header>
                <n-h4>Modélisation</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  UML&nbsp;/ SysML&nbsp;/ Merise
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing>
              <template #header>
                <n-h4>Bases de Données</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  MySQL&nbsp;/ MariaDB&nbsp;/<br>
                  MongoDB&nbsp;/ SQLite
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
          <n-list-item>
            <n-thing>
              <template #header>
                <n-h4>Outils Logiciels</n-h4>
              </template>
              <template #header-extra>
                <n-p>
                  Figma&nbsp;/ Git&nbsp;/ Docker&nbsp;/<br>
                  npm&nbsp;/ Yarn&nbsp;/ Composer
                </n-p>
              </template>
            </n-thing>
          </n-list-item>
        </n-list>
      </div>
    </div>
  </section>
</template>

<style scoped lang="postcss">
.card {
  @apply bg-gray-600/90 border rounded-md border-purple px-6 mx-auto mb-10 flex flex-col w-full md:w-2/3 lg:w-[45%] max-w-md;
}
.card-title {
  @apply border-b border-purple py-5 mb-0 text-center text-lg md:text-xl xl:text-2xl;
}
.n-h4 {
  @apply m-0 text-base md:text-lg xl:text-xl;
}
.n-p {
  @apply py-2 pl-2 text-sm md:text-base xl:text-[1.1rem];
}
.n-thing-header .n-p {
  @apply text-right;
}
</style>