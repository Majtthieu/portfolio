<template>
  <main>
    <div v-if="projectData" class="project-container">
      <h3>Projet {{ projectData.title }}</h3>
      <div class="projects-title_line"></div>
      <div class="project-main">
        <div class="project-images">

          <img class="project-images_dt" :src="`${baseUrl}assets/images/${projectImages[0]}`" :alt="projectData.title" />


          <img class="project-images_mb" :src="`${baseUrl}assets/images/${projectImages[1]}`" :alt="projectData.title" />

        </div>
        <div class="project-text">
          <p class="long-text">{{ projectData.longdesc }}</p>
          <div class="project-text_links">
            <a :href="projectData.github" target="_blank"><img src="@/assets/images/icos/github.svg" alt="icone Github" />
              lien repo Github</a>
            <a v-if="projectData.demo" :href="projectData.demo" target="_blank"><img src="@/assets/images/icos/world.svg"
                alt="icone WWW" />
              lien démo</a>
          </div>
          <div class="project-text_technologies">
            <span>Principales technos utilisées : </span>
            <span class="tags" v-for="(technology, index) in projectData.technologies" :key="index">{{ technology
            }}</span>
          </div>
        </div>
      </div>
      <div class="project-nav">
        <button @click="$router.push('/#projects-anchor')" id="back-to-projects"
          class="button_global button_contact">Retour aux
          projets</button>
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
      this.projectImages = project.images;
    } else {
      this.$router.push('/404');
    }
  },
};
</script>
  
<style scoped>
@import "./ProjectView.sass";
</style>
  