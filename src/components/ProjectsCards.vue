<script setup>
import projects from '../datas/projects.json'
</script>

<template>
    <div class="projects-container">
        <div class="projects-title">
            <h3 id="projects-anchor">Projets</h3>
            <div class="projects-title_line"></div>
        </div>
        <div class="projects-cards">
            <router-link v-for="(project, index) in projects" :key="project.id" :to="`/project/${project.id}`"
                class="projects-card" :class="{ 'projects-card_reverse': index % 2 !== 0 }"><!-- class supplémentaire pour inverser texte et image à chaque card -->
                <div class="projects-card_text">
                    <h4>{{ project.title }}</h4>
                    <p>{{ project.description }}</p>
                    <div class="projects-card_text_technologies">
                        <span v-for="(technology, index) in project.technologies" :key="index">{{ technology }}</span>
                    </div>
                </div>
                <div class="projects-card_image">
                    <img :src="`${baseUrl}src/assets/images/${project.cover}`" :alt="project.title">
                </div>
            </router-link>
        </div>
    </div>
</template>

<script>
export default {
  computed: {
    baseUrl() {
      return import.meta.env.BASE_URL;
    }
  }
};
</script>

  <style scoped>
  @import "./ProjectsCards.sass";
  </style>