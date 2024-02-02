<script setup>
</script>

<template>
  <div class="welcome">
    <div class="welcome-text">
      <p class="welcome-text_hello">Bonjour, je m'appelle</p>
      <h1 class="welcome-text_name">Matthieu Jankowiak</h1>
      <h2>Développeur Web</h2>
      <p class="welcome-text_addition">Découvrez mes projets et n'hésitez pas à me contacter pour évoquer notre future
        collaboration</p>
      <div class="welcome-text_buttons">
        <a href="#projects-anchor" class="button_global button_projects">Projets</a>
        <button class="button_global button_contact" @click="$router.push('/contact')">Contact</button>
        <!-- <a  download="fake_cv.pdf" href="@/assets/fake_cv.pdf">--><button class="button_global button_resume"><img src="@/assets/images/icos/save.svg" alt="icone téléchargement"/>CV</button><!--</a> -->
      </div>
    </div>
    <div class="welcome-illustration">
      <img src="@/assets/images/pexels-fauxels-3184416.webp" alt="deux personnes dont une serre la main à quelqu'un hors-champ">
    </div>
    <svg id="path" xmlns="http://www.w3.org/2000/svg" style="position:absolute">
      <defs>
        <clipPath id="mask">
          <path d="M86,0c19,20.2,80.5,90.7,85,197c5.3,125.8-130.4,198.7-136,268c-2,24.6,19,50.8,50,73c21,15,65,36,121,48
	c133.9,28.7,349.1,2.5,434,5c-46-334.1,0-394,0-591H86z"/>
        </clipPath>
        <clipPath id="mask-s">
          <path d="M86,0c19,20.2,114.5,108.6,119,214.9c5.3,125.8-50,148-88,223c-19,38-29,71.9-14,102c25,37.9,56,43.9,115,52
	c142,12.9,337.1-3.4,422-0.9c-46-334.1,0-394,0-591H86z"/>
</clipPath>
      </defs>

    </svg>
  </div>
</template>

<style scoped>
@import "./TheWelcome.sass";
</style>
