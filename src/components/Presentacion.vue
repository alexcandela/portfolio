<template>
  <div id="presentacion" class="presentacion section">
    <div class="presentacion-img">
      <img src="/src/assets/images/alex3recortada.jpg" alt="profile_img">
    </div>
    <div class="presentacion-info">
      <div class="presentacion-info-nombre">
        <h1 v-if="translate">Hi, im <span>Alex Candela</span></h1>
        <h1 v-else>Hola, soy <span>Alex Candela</span></h1><img src="/src/assets/images/bot.png" alt="bot">
      </div>
      <div class="presentacion-info-desc">
        <p v-if="translate">Curious by nature and meticulous by choice, I strive to learn something new every day and
          dedicate myself to ensuring that every detail reaches perfection.</p>
        <p v-else>Curioso por naturaleza y meticuloso por elección, me esfuerzo por aprender algo nuevo cada día y me
          dedico a que cada detalle alcance la perfección.
        </p>
      </div>
      <div class="presentacion-info-botones">
        <a href="https://www.linkedin.com/in/alex-candela-b31956228/" target="blank" class="btn btn-linkedin"><i
            class="fa-brands fa-linkedin"></i>Linkedin</a>
        <a target="blank" href="https://github.com/alexcandela" class="btn btn-github"><i
            class="fa-brands fa-github"></i>Github</a>
        <a href="/CV_AlexCandela.pdf" download class="btn btn-resume"><i class="fa-solid fa-file"></i>Resume</a>
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