<script setup>
import { ref } from "vue"

const isOpen = ref(false)
</script>

<template>
  <nav class="navbar fixed-top" id="mainNav">
    <div class="container nav__container">
      <!-- Logo -->
      <a class="proyectonombre" href="#">
        <span class="titulonavbar">mi</span>
        <span class="titulonavbar2">Portafolio</span>
      </a>

      <!-- Botón DarkMode mobile 
      <button class="darkModeSwitch d-lg-none" id="switch-mobile">
        <i class="bx bx-sun"></i>
        <i class="bx bx-moon"></i>
      </button>-->

      <!-- Botón hamburguesa -->
      <button
        class="navbar-toggler"
        type="button"
        @click="isOpen = !isOpen"
        :aria-expanded="isOpen.toString()"
        aria-controls="navbarResponse"
        aria-label="Toggle navigation"
      >
        ☰
      </button>

      <!-- Menú -->
      <div
        id="navbarResponse"
        class="navbar-menu"
        :class="{ open: isOpen }"
      >
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link lead" href="#sobre-mi">Sobre mí</a></li>
          <li class="nav-item"><a class="nav-link lead" href="#experiencia">Experiencia</a></li>
          <li class="nav-item"><a class="nav-link lead" href="#estudios">Mis estudios</a></li>
          <li class="nav-item"><a class="nav-link lead" href="#proyectos">Proyectos</a></li>
          <li class="nav-item"><a class="nav-link lead" href="#contacto">Contactame</a></li>
        </ul>

        <!-- Botón DarkMode desktop 
        <button class="darkModeSwitch d-none d-lg-inline" id="switch-desktop">
          <i class="bx bx-sun"></i>
          <i class="bx bx-moon"></i>
        </button>-->
      </div>
    </div>
  </nav>
</template>

<style scoped>
/* Navbar base */
.navbar {
  background-color: #000;
  padding: 0.5rem 1rem;
  z-index: 999;
}

.nav__container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* Logo "miPortafolio" */
.proyectonombre {
  font-size: 1.5rem;
  font-weight: bold;
  text-decoration: none;
}

.titulonavbar {
  color: #fff;
}

.titulonavbar2 {
  color: var(--gold1, #f4bd76);
}

/* Botones Dark Mode */
.darkModeSwitch {
  border: none;
  background: none;
  font-size: 1.5rem;
  color: white;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 0.3rem;
}

/* Botón hamburguesa */
.navbar-toggler {
  background: none;
  border: none;
  font-size: 1.8rem;
  color: white;
  cursor: pointer;
}

/* Menú */
.navbar-menu {
  display: none;
  flex-direction: column;
  gap: 0.8rem;
  margin-top: 1rem;
  text-align: center;
}

/* Menú abierto en mobile */
.navbar-menu.open {
  display: flex;
}

/* En desktop: siempre visible y horizontal */
@media (min-width: 992px) {
  .navbar-menu {
    display: flex !important;
    flex-direction: row;
    align-items: center;
    margin-top: 0;
    gap: 1rem;
  }

  .navbar-toggler {
    display: none;
  }
}

/* Links */
.navbar-nav {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
  padding: 0;
  margin: 0;
}

@media (min-width: 992px) {
  .navbar-nav {
    flex-direction: row;
    gap: 1rem;
  }
}

.nav-link {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.2s;
}

.nav-link:hover {
  color: var(--gold1, #f4bd76);
}
</style>
