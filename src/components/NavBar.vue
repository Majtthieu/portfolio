<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
<header>
  <div class="name">
    <RouterLink to="/">
    <p>Matthieu Jankowiak</p>
  </RouterLink>
  </div>
  <div class="nav-wrapper">
      <nav>
        <RouterLink to="/">Accueil</RouterLink>
        <RouterLink to="/about">Qui suis-je</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>
    <!-- <div class="resume-wrapper">
    <a class="resume" download="fake_cv.pdf" href="@/assets/fake_cv.pdf">CV</a>
    <i></i>
    </div> -->
  </header>

  <RouterView />
</template>

<style scoped>
@import "./NavBar.sass";
</style>