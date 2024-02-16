<script setup>
import projects from '../datas/projects.json'
</script>

<template>
  <div class="projects-container">
    <div class="projects-title">
      <h3 id="projects-anchor">Mes derniers projets</h3>
      <div class="projects-title_line"></div>
    </div>
    <div class="projects-cards">
      <Splide
        :options="{ rewind: true, perPage: 3, perMove: 2, arrows: true, pagination: false, lazyLoad: 'sequential', breakpoints: { 1280: { perPage: 2, perMove: 1 }, 768: { perPage: 1, perMove: 1 } } }"
        aria-label="carousel de mes derniers projets" :has-track="false">
        <SplideTrack>
          <SplideSlide v-for="(project) in projects" :key="project.id">
            <router-link :to="`/project/${project.id}`" class="projects-card">
              <div class="projects-card_image">
                <img :data-splide-lazy="`/images/${project.cover}`" :alt="project.title">
              </div>
              <div class="projects-card_text">
                <h4>{{ project.title }}</h4>
                <p>{{ project.shortdesc }}<br>{{ project.shortdescadd }}</p>
                <div class="projects-card_text_technologies">
                  <span class="tags" v-for="(technology, index) in project.technologies" :key="index">{{ technology
                  }}</span>
                </div>
              </div>
            </router-link>
          </SplideSlide>
        </SplideTrack>
        <div class="splide__arrows">
          <button class="splide__arrow splide__arrow--prev"><svg id="svgp" clip-rule="evenodd" fill-rule="evenodd"
              stroke-linejoin="round" stroke-miterlimit="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path
                d="m12.007 2c-5.518 0-9.998 4.48-9.998 9.998 0 5.517 4.48 9.997 9.998 9.997s9.998-4.48 9.998-9.997c0-5.518-4.48-9.998-9.998-9.998zm1.523 6.21s1.502 1.505 3.255 3.259c.147.147.22.339.22.531s-.073.383-.22.53c-1.753 1.754-3.254 3.258-3.254 3.258-.145.145-.335.217-.526.217-.192-.001-.384-.074-.531-.221-.292-.293-.294-.766-.003-1.057l1.977-1.977h-6.693c-.414 0-.75-.336-.75-.75s.336-.75.75-.75h6.693l-1.978-1.979c-.29-.289-.287-.762.006-1.054.147-.147.339-.221.53-.222.19 0 .38.071.524.215z"
                fill-rule="nonzero" />
            </svg></button>
          <button class="splide__arrow splide__arrow--next"><svg id="svgn" clip-rule="evenodd" fill-rule="evenodd"
              stroke-linejoin="round" stroke-miterlimit="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path
                d="m12.007 2c-5.518 0-9.998 4.48-9.998 9.998 0 5.517 4.48 9.997 9.998 9.997s9.998-4.48 9.998-9.997c0-5.518-4.48-9.998-9.998-9.998zm1.523 6.21s1.502 1.505 3.255 3.259c.147.147.22.339.22.531s-.073.383-.22.53c-1.753 1.754-3.254 3.258-3.254 3.258-.145.145-.335.217-.526.217-.192-.001-.384-.074-.531-.221-.292-.293-.294-.766-.003-1.057l1.977-1.977h-6.693c-.414 0-.75-.336-.75-.75s.336-.75.75-.75h6.693l-1.978-1.979c-.29-.289-.287-.762.006-1.054.147-.147.339-.221.53-.222.19 0 .38.071.524.215z"
                fill-rule="nonzero" />
            </svg></button>
        </div>
      </Splide>
    </div>
  </div>
</template>

<script>
import { Splide, SplideSlide, SplideTrack } from '@splidejs/vue-splide';

export default {
  components: {
    Splide,
    SplideSlide,
    SplideTrack
  },
};
</script>

<style scoped>@import "./ProjectsCards.sass";</style>