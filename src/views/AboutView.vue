<script setup>

</script>

<template>
  <main>
    <div class="about">
      <div class="about-text">
        <h3>À propos de moi</h3>
        <div class="projects-title_line"></div>
        <p class="long-text">Le développement web me fascine par sa créativité et sa diversité. Je viens de réussir une
          formation dans ce domaine avec OpenClassrooms (<a
            href="https://static.oc-static.com/syllabus/899-developpeur-web-fr-fr-standard.pdf" target="_blank"
            class="program-link">pdf du programme</a>). J'ai travaillé sur plusieurs projets
          qui m'apportent de solides bases en Front-end et back-end. Je suis également à l’aise avec les outils de gestion
          de version comme Git et GitHub.<br>Mais ce n’est pas tout ! Fort de mon expérience antérieure, je possède des
          compétences interpersonnelles indispensables pour travailler en équipe. Je sais communiquer efficacement,
          m’adapter aux situations, et résoudre les problèmes. Mon CV vous en dira plus sur mon parcours et mes
          réalisations. Je suis convaincu que je peux apporter une valeur ajoutée à votre entreprise, grâce à ma
          motivation, ma curiosité et ma capacité d’apprentissage. Je serais ravi de discuter de votre projet et de vos
          besoins. N'hésitez pas à me contacter.
        </p>
        <a class="button_global button_resume" download="cv-jankowiak.pdf" href="/cv-jankowiak.pdf"><img
            src="@/assets/images/icos/save.svg" alt="icone téléchargement" />CV</a>
      </div>
      <div class="about-illustrations">
        <div class="about-illustrations_image">
          <img src="@/assets/images/portrait.png" alt="portrait Matthieu Jankowiak">
        </div>
        <h4>Mes compétences</h4>
        <div class="skills">
          <span class="skills-techno">HTML</span>
          <span class="skills-techno">CSS</span>
          <span class="skills-techno">JavaScript</span>
          <span class="skills-techno">React</span>
          <span class="skills-techno">Vue</span>
          <span class="skills-techno">Node</span>
          <span class="skills-techno">Express</span>
          <span class="skills-techno">MongoDB</span>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>@import "./AboutView.sass";</style>