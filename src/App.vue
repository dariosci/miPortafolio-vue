<script setup>
  import navBar from './components/navBar.vue';
  import sobreMi from './components/icons/sobreMi.vue';
  import miExperiencia from './components/icons/miExperiencia.vue';
  import misEstudios from './components/icons/misEstudios.vue';
  import misProyectos from './components/icons/misProyectos.vue';
  import miContacto from './components/miContacto.vue';
  import footerVue from './components/footerVue.vue';
</script>

<template>
  <header>
    <navBar />
  </header>
  <main>    
    <sobreMi />
    <miExperiencia />
    <misEstudios />
    <misProyectos />
    <miContacto />
    <footerVue />
  </main>
</template>

<style scoped>

</style>
