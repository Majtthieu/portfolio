<script setup>
</script>

<template>
  <div class="welcome">
    <div class="welcome-text">
      <h2>Développeur Web</h2>
      <p class="welcome-text_hello">Bonjour, je m'appelle</p>
      <h1 class="welcome-text_name">Matthieu Jankowiak</h1>
      <p class="welcome-text_addition">Découvrez mes projets et n'hésitez pas à me contacter pour évoquer notre future
        collaboration</p>
      <div class="welcome-text_buttons">
        <a href="#projects-anchor" class="button_global button_projects">Projets</a>
        <button class="button_global button_contact" @click="$router.push('/contact')">Contact</button>
        <!-- <a  download="fake_cv.pdf" href="@/assets/fake_cv.pdf">--><button class="button_global button_resume"><img src="@/assets/images/icos/save.svg"/>CV</button><!--</a> -->
      </div>
    </div>
    <div class="welcome-illustration">
      <img src="@/assets/images/pexels-fauxels-3184416.png" alt="deux personnes dont une serre la main à quelqu'un hors-champ">
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" style="position:absolute">
      <defs>
        <clipPath id="mask">
          <path d="M86,0c19.01,20.22,80.51,90.7,85,197c5.32,125.84-130.41,198.73-136,268c-1.99,24.61,18.97,50.84,50,73c21,15,65,36,121,48
	c133.89,28.69,349.14,2.47,434,5c0-197,0-394,0-591H86z"/>
        </clipPath>
      </defs>

    </svg>
  </div>
</template>

<style scoped>
@import "./TheWelcome.sass";
</style>
   
```
