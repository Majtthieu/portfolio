<template>
    <div class="project-container">
      <h3 v-if="projectData">Projet {{ projectData.title }}</h3>
      <!-- <p>{{ projectData.description }}</p> -->
    </div>
  </template>
  
  <script>
  import projects from '../datas/projects.json';
  
  export default {
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
  
  <style scoped>
  @import "./ProjectView.sass";
  </style>
  