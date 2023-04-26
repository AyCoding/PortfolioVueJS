<script setup>
import ProjectItem from "@/components/ProjectItem.vue";

const projects = [
    {
        name: 'CV en ligne',
        language: 'HTML / CSS',
        link: 'https://aycoding.github.io/',
        year: 2022
    },
    {
        name: 'Portfolio',
        language: 'HTML / CSS',
        link: 'https://aycoding.github.io/Portfolio/',
        year: 2022
    },
    {
        name: 'Web Sage-femme',
        language: 'HTML / CSS / JS',
        link: 'https://canaud-emilie-sage-femme.fr/',
        year: 2022
    },
    {
        name: 'Sélection (Lycée Monge)',
        language: 'PHP / MySQL',
        link: 'https://github.com/AyCoding/Projet-Selection',
        year: 2022
    },
    {
        name: 'Portfolio VueJS',
        language: 'Vue.js',
        link: '/',
        year: 2023
    }
]
</script>

<template>

  <section class="projects">
      <ProjectItem v-for="project in projects"
                   :lang="project.language"
                   :link="project.link"
                   :year="project.year">
          {{ project.name }}
      </ProjectItem>
  </section>

</template>

<style scoped>

.projects {
    display: flex;
    justify-content: center;
    flex-flow: wrap;
    gap: 30px;
    margin: 50px auto;
}

</style>