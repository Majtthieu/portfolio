<script setup>

</script>

<template>
  <main>
    <div class="about">
      <div class="about-text">
        <h3>À propos de moi</h3>
        <div class="projects-title_line"></div>
        <p class="long-text">
          En transition professionnelle, je viens de me former avec OpenClassrooms pour me positionner en tant que
          développeur débutant. Toutefois, mes compétences interpersonnelles,
          forgées au fil de mon parcours professionnel, constituent un atout majeur.
          Mon CV témoigne de ces compétences. J'ai toujours allié efficacement le travail en autonomie et en équipe,
          démontrant une capacité d'adaptation et de résolution de problèmes. Bien que mes compétences techniques soient
          en évolution, ma solide compréhension du monde professionnel me permet d'apporter une valeur ajoutée à toute
          équipe. N'hésitez pas à me contacter pour en discuter davantage.
        </p>
        <button class="button_global button_resume"><img src="@/assets/images/icos/save.svg"
            alt="icone téléchargement" />CV</button>
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

<style scoped>
@import "./AboutView.sass";
</style>