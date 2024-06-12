<template>
  <div id="proyectos" class="proyectos section">
    <div class="titulo">
      <div class="titulo-text">
        <h3 v-if="translate">Projects</h3>
        <h3 v-else>Proyectos</h3> <img src="/src/assets/images/iconos/star.svg" alt="star">
      </div>
      <div class="titulo-hr">
        <hr>
      </div>
    </div>
    <div class="proyectos-lista">
      <div class="proyectos-lista-proyecto">
        <div class="img">
          <a target="blank" href="https://2048-henna.vercel.app/"><img src="/src/assets/images/captura2048.png"
              alt="2048"></a>
        </div>
        <div class="info">
          <div class="info-titulo">2048 Game</div>
          <div v-if="translate" class="info-desc">Clone of the 2048 game. A puzzle game where you combine numbered tiles
            to reach the number 2048.</div>
          <div v-else class="info-desc">Clon del juego 2048. Juego de puzzle donde combinas baldosas numeradas para
            alcanzar la cifra 2048.
          </div>

          <div class="info-tech"><i class="fa-brands fa-html5 html"></i><i class="fa-brands fa-css3-alt css"></i><i
              class="fa-brands fa-vuejs vue"></i><i class="fa-brands fa-sass sass"></i></div>
        </div>
      </div>
      <div class="proyectos-lista-proyecto">
        <div class="img">
          <a target="blank" href="https://www.youtube.com/watch?v=IEj1uqlGZK0&t=1s"><img
              src="/src/assets/images/eventium.png" alt="2048"></a>
        </div>
        <div class="info">
          <div class="info-titulo">Eventium</div>
          <div v-if="translate" class="info-desc">Simulation of a web application where you can publish events and attend them.</div>
          <div v-else class="info-desc">Simulación de aplicación web donde se pueden publicar eventos y asistir a ellos.</div>
          <div class="info-tech"><i class="fa-brands fa-html5 html"></i><i class="fa-brands fa-css3-alt css"></i><i
              class="fa-brands fa-laravel laravel"></i><i class="fa-brands fa-js js"></i><i
              class="fa-brands fa-sass sass"></i></div>
        </div>
      </div>
      <div class="proyectos-lista-proyecto">
        <div class="img">
          <a target="blank" href="https://www.youtube.com/watch?v=ksYQlPEz_BM"><img
              src="/src/assets/images/capturaBorsa.png" alt="2048"></a>
        </div>
        <div class="info">
          <div v-if="translate" class="info-titulo">Job Board</div>
          <div v-else class="info-titulo">Bolsa de trabajo</div>
          <div v-if="translate" class="info-desc">Job board for my institute, to publish and apply for internship opportunities.
          </div>
          <div v-else class="info-desc">Bolsa de trabajo para mi instituto, para publicar e inscribirse a ofertas de practicas.
          </div>
          <div class="info-tech"><i class="fa-brands fa-html5 html"></i><i class="fa-brands fa-css3-alt css"></i><i
              class="fa-brands fa-vuejs vue"></i><i class="fa-brands fa-sass sass"></i><i
              class="fa-brands fa-laravel laravel"></i></div>
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