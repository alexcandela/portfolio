<template>
  <div id="tecnologias" class="tecnologias section">
    <div class="titulo">
      <div class="titulo-text">
        <h3 v-if="translate">Technologies</h3>
        <h3 v-else>Tecnologías</h3><img src="/src/assets/images/iconos/code.svg" alt="star">
      </div>
      <div class="titulo-hr">
        <hr>
      </div>
    </div>
    <div class="tecnologias-lista">
      <div class="tech">
        <div class="tech-titulo">
          <h4>Back End</h4>
        </div>
        <div class="tech-tecnologias">
          <i class="fa-brands fa-php php"></i>
          <i class="fa-brands fa-laravel laravel"></i>
        </div>
      </div>
      <div class="tech">
        <div class="tech-titulo">
          <h4>Front End</h4>
        </div>
        <div class="tech-tecnologias">
          <i class="fa-brands fa-html5 html"></i>
          <i class="fa-brands fa-css3-alt css"></i>
          <i class="fa-brands fa-js js"></i>
          <i class="fa-brands fa-vuejs vue"></i>
          <i class="fa-brands fa-angular angular"></i>
        </div>
      </div>
      <div class="tech">
        <div class="tech-titulo">
          <h4 v-if="translate">Design</h4>
          <h4 v-else>Diseño</h4>
        </div>
        <div class="tech-tecnologias">
          <i class="fa-brands fa-figma figma"></i>
          <i class="fa-solid fa-basketball dribble"></i>
        </div>
      </div>
      <div class="tech">
        <div class="tech-titulo">
          <h4 v-if="translate">Tools</h4>
          <h4 v-else>Herramientas</h4>
        </div>
        <div class="tech-tecnologias">
          <i class="fa-brands fa-github github"></i>
          <i class="fa-brands fa-gitlab gitlab"></i>
          <i class="fa-brands fa-docker docker"></i>
        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

let translate = ref(false);

const toggleTranslate = () => {
  translate.value = !translate.value;
}

defineExpose({
  toggleTranslate
});
</script>

<style></style>