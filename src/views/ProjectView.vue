<template>
  <main>
  <div v-if="projectData" class="project-container">
    <h3>Projet {{ projectData.title }}</h3>
    <div class="projects-title_line"></div>
    <div class="project-main">
      <div class="project-images">
        <img :src="`${baseUrl}src/assets/images/${projectData.cover}`" :alt="projectData.title">
      </div>
      <div class="project-text">
        <p class="long-text">Il s'agissait d'intégrer une maquette pour une application de location immobilière, avec l'utilisation de React et un design responsive. J'ai donc créé l'application React avec ses routes (gestion des routes inexistantes incluse) et ses composants, par exemple un slider et des éléments collapsibles. L'utilisation de Sass a permis l'adaptation du design aux différentes tailles d'écran grâce à l'utilisation de variables et de mixins. Pour ce projet, une démo déployée sur Vercel est disponible</p>
        <div class="project-text_links">
          <a :href="projectData.github" target="_blank"><img src="@/assets/images/icos/github.svg" alt="icone Github"/> lien repo Github</a>
          <a v-if="projectData.demo" :href="projectData.demo" target="_blank"><img src="@/assets/images/icos/world.svg" alt="icone WWW"/>
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
</main>
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
  