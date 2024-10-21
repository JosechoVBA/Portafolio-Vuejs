<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/Educacion.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponente from './components/ProyectosComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';
</script>

<template>
  <Header id="top">
    <!--Barra de Navegacion-->
    <NavBar/>
    <!--Componente Datos Personales-->
    <DatosPersonales />
  </Header>
  <main>
      <!--el estilo CSS de Section se encuentra en base.css-->
      <section id="educacion"><h2>Educación - Cursos</h2>
      <!--Componente Educacion-->
        <Educacion/>
      </section>
      <section id="experiencia"><h2>Experiencia</h2>
        <!--Componente Experiencia-->
      <ExperienciaComponente/>
      </section>
      <section id="proyectos">
        <h2>Proyectos</h2>
        <!--Componente Proyectos-->
        <ProyectosComponente/>
      </section>
      <section id="habilidades">
        <!--Componente Habilidades-->
        <h2>Habilidades</h2>
        <HabilidadesComponente/>
      </section>
      <section id="intereses">
        <!--Componente Intereses-->
        <h2>Intereses</h2>
        <InteresesComponente />
      </section>
  </main>
  <footer>
    <a href="#top">Inicio</a>
    <p>©️ 2024 Jose Luis Villalba - Portafolio Web</p>
  </footer>
</template>

<style scoped>
footer{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
}
</style>
