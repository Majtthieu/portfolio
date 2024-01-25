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
  </header>

  <RouterView />
</template>

<style scoped>
@import "./NavBar.sass";
</style>