<template>
  <div v-if="projectData" class="project-container">
    <h3>Projet {{ projectData.title }}</h3>
    <div class="projects-title_line"></div>
    <div class="project-main">
      <div class="project-images">
        <img :src="`${baseUrl}src/assets/images/${projectData.cover}`" :alt="projectData.title">
      </div>
      <div class="project-text">
        <p class="long-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ultricies felis quis erat
          cursus, non tincidunt mauris convallis. Vivamus ac arcu non quam varius tincidunt sit amet id metus. Morbi eu
          lectus at nunc dignissim bibendum. Nunc congue dolor et vestibulum dapibus. Nulla facilisi. Sed gravida purus ac
          tellus cursus, vitae varius justo consequat. Integer auctor, dui et feugiat lacinia, elit eros tincidunt tortor,
          vel fermentum libero felis vel nisl. Proin sollicitudin cursus tellus, ut aliquet justo consequat ut. Fusce
          eleifend augue vitae quam rhoncus, in dignissim justo fermentum.</p>
        <div class="project-text_links">
          <a :href="projectData.github" target="_blank"><img src="@/assets/images/icos/github.svg" /> lien repo Github</a>
          <a v-if="projectData.demo" :href="projectData.demo" target="_blank"><img src="@/assets/images/icos/world.svg" />
            lien démo</a>
        </div>
        <div class="project-text_technologies">
          <span>Principales technos utilisées : </span>
          <span class="tags" v-for="(technology, index) in projectData.technologies" :key="index">{{ technology }}</span>
        </div>
      </div>
    </div>
    <div class="project-nav">
      <router-link to="/#projects-anchor"><button id="back-to-projects" class="button_global button_contact">Retour aux
          projets</button></router-link>
    </div>

  </div>
</template>
  
<script>
import projects from '../datas/projects.json';

export default {
  computed: {
    baseUrl() {
      return import.meta.env.BASE_URL;
    }
  },
  data() {
    return {
      projectData: null,
    };
  },
  mounted() {
    const routeId = this.$route.params.id;
    const project = projects.find((project) => project.id === routeId);
    if (project) {
      this.projectData = project;
    } else {
      this.$router.push('/404');
    }
  },
};


</script>
  
<style scoped>@import "./ProjectView.sass";</style>
  