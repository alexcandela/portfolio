<template>
  <header>
    <div class="options">
      <div class="darkMode">
        <i class="fa-solid fa-moon"></i>
        <label class="switch">
          <input type="checkbox">
          <span class="slider"></span>
        </label>
        <i class="fa-solid fa-sun"></i>
      </div>
      <div class="idioma">
        <span>Español</span>
        <label class="switch">
          <input type="checkbox">
          <span class="slider"></span>
        </label>
        <span>English</span>
      </div>
    </div>
    <div class="links">
      <div class="links-btn">
        <i class="fa-solid fa-circle-user"></i>
        <a href="http://">Sobre Mí</a>
      </div>
      <div class="links-btn">
        <i class="fa-solid fa-star"></i>
        <a href="http://">Proyectos</a>
      </div>
      <div class="links-btn">
        <i class="fa-solid fa-briefcase"></i>
        <a href="http://">Experiencia</a>
      </div>
      <div class="links-btn">
        <i class="fa-solid fa-code"></i>
        <a href="http://">Tecnologías</a>
      </div>
    </div>
  </header>

  <main>
    <Presentacion />
    <Proyectos />
    <Experiencias />
    <Tecnologias />
  </main>
</template>
<script setup>
import Presentacion from "./components/Presentacion.vue";
import Proyectos from "./components/Proyectos.vue";
import Experiencias from "./components/Experiencia.vue";
import Tecnologias from "./components/Tecnologias.vue";

</script>
<style scoped>
/* Estilos base del switch */
.switch {
  position: relative;
  display: inline-block;
  width: 40px;
  height: 20px;
}

/* Estilos del input */
.switch input {
  display: none;
}

/* Estilos del slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  transition: .4s;
  border-radius: 20px;
}

/* Estilos del slider cuando está activado */
.slider:before {
  position: absolute;
  content: "";
  height: 16px;
  width: 16px;
  left: 2px;
  bottom: 2px;
  background-color: white;
  transition: .4s;
  border-radius: 50%;
}

/* Estilos del slider cuando está activado */
input:checked+.slider {
  background-color: #2196F3;
}

/* Estilos del slider cuando está activado */
input:checked+.slider:before {
  transform: translateX(20px);
}
</style>
