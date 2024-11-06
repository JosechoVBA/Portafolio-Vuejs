<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import icono1 from '/src/assets/experiencia1.svg';
import icono2 from '/src/assets/experiencia2.svg';
import icono3 from '/src/assets/experiencia1.svg';
import icono4 from '/src/assets/experiencia2.svg';
import { ref } from "vue";

const titulo = 'Data Analytics';
const fecha = 'Desde Enero 2017 hasta la fecha';
const experiencias = ref([
  {
    id: 1,
    src: icono1,
    parrafo: 'Lideré un equipo de analistas enfocados en la recopilación de datos de diversas fuentes de información los cuales empleaban diversos software (s) para el resumen de grandes volúmenes de datos y la obtención de conocimiento'
  },
  {
    id: 2,
    src: icono2,
    parrafo: 'Me desempeñe como analista estratégico en un Centro de Análisis Criminal, desde el cual desarrollé diversos estudios estratégicos prospectivos, empleando análisis estadísticos y técnicas de estudios prospectivos'
  },
  {
    id: 3,
    src: icono3,
    parrafo: 'Me desempeñe como analista táctico de fuentes de información abiertas sobre los cuales creaba diversos paneles de visualización para la muestra de resultados'
  },
  {
    id: 4,
    src: icono4,
    parrafo: 'Me desempeñe como capacitador en diversos cursos y seminarios de Data Analysis'
  }
]);
</script>


<template>
  <div class="card">
    <h3 class="titulo">{{ titulo }}</h3>
    <p class="fecha">{{ fecha }}</p>
    <ul class="listado">
      <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
        <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo" />
        <p>{{ experiencia.parrafo }}</p>
      </li>
    </ul>
  </div>
</template>


<style scoped>
    .card{
        display: flex;
        flex-direction: column;
        padding: 2rem;
        background-color: rgb(28, 41, 52);
        border-radius: 15px;
    }

    .titulo {
        font-size: 1.5rem;
        color: coral;
    }

  .fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
  }

  .listado {
    display: flex;
    flex-direction: column;
  }

  .item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
  }
</style>

