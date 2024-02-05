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
	c119.5,25.6,303.8,7.5,402.4,5.1c16.8-0.4,29.5-15.2,27.4-31.9C596.9,252.9,640,190.6,640,0H86z"/>
        </clipPath>
        <clipPath id="mask-s">
          <path d="M85.9,0c19,20.2,123.6,95.7,128.1,202c5.3,125.8-93,226-117,262c-11.1,19.9-18,52,4,82
	c18,19.9,48.9,28,104.9,40c119.5,25.6,303.8,7.5,402.4,5.1c16.8-0.4,31.6-15.1,31.6-31.9c0.2-301.2,0-368.6,0-559.2L85.9,0L85.9,0z"/>
</clipPath>
      </defs>

    </svg>
  </div>
</template>

<style scoped>
@import "./TheWelcome.sass";
</style>
