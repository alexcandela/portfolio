<template>
  <div id="experiencias" class="experiencias section">
    <div class="titulo">
      <div class="titulo-text">
        <h3 v-if="translate">Experiences</h3>
        <h3 v-else>Experiencia</h3> <img src="/src/assets/images/iconos/exp.svg" alt="experiencia">
      </div>
      <div class="titulo-hr">
        <hr>
      </div>
    </div>
    <div class="experiencias-lista">
      <div class="exp">
        <div class="exp-titulo">
          <h3>Web Developer · Holzadac</h3><img src="/src/assets/images/about.png" alt="about">
        </div>
        <div class="exp-desc">
          <p v-if="translate">Web developer using WordPress. My work involved creating custom designs, implementing
            plugins for courses and stores, ensuring security, and optimizing site performance. I succeeded in enhancing
            user experience and contributing to the success of several web projects.</p>
          <p v-else>Desarrollador web utilizando WordPress. Mi trabajo incluía crear diseños personalizados, implementar
            plugins para cursos y tiendas, garantizar la seguridad y optimizar el rendimiento de los sitios. Logré
            mejorar la experiencia del usuario y contribuir al éxito de varios proyectos web.</p>
          <img src="/src/assets/images/ai.png" alt="computer">
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
