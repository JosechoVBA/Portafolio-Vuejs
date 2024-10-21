<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';

// Definir los intereses como un array reactivo
const intereses = ref([
  "Desarrollo de Software de código abierto. Contribuyo a proyectos en GitHub.",
  "Deportes al aire libre: disfruto de carreras y senderismo al aire libre. Practico y entreno Padel regularmente con amigos.",
  "Música: Practico guitarra como hobby, lo que me gusta mucho como momento de relajación y distensión."
]);
</script>

<template>
  <div class="intereses-contenedor">
    -<FondoLava />
    <ul class="contenedor-lista">
      <li v-for="(interes, index) in intereses" :key="index" class="item">
        {{ interes }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.intereses-contenedor{
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista{
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item{
    margin-bottom: 1rem;
}
</style>