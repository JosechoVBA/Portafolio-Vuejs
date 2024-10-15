<script setup>
const skillsData = [
  {
    categoria: 'Lenguajes de Programacion',
    habilidades: [
      { nombre: 'JavaScript', nivel: 'Intermedio', icono: '/src/components/icons/js.svg' },
      { nombre: 'Python', nivel: 'Intermedio', icono: '/src/components/icons/python.svg' },
      { nombre: 'HTML/CSS', nivel: 'Intermedio', icono: '/src/components/icons/html-css.svg' },
      { nombre: 'Java', nivel: 'Intermedio', icono: '/src/components/icons/java.svg' },
      { nombre: 'SQL', nivel: 'Intermedio', icono: '/src/components/icons/sql.svg' }
    ]
  },
  {
    categoria: 'Frameworks y Librerias',
    habilidades: [
      { nombre: 'React.js', nivel: 'Intermedio', icono: '/src/components/icons/react.svg' },
      { nombre: 'Vue.js', nivel: 'Intermedio', icono: '/src/components/icons/vue.svg' },
      { nombre: 'Node.js', nivel: 'Intermedio', icono: '/src/components/icons/node.svg' },
      { nombre: 'Django', nivel: 'Intermedio', icono: '/src/components/icons/django.svg' },
      { nombre: 'Bootstrap', nivel: 'Intermedio', icono: '/src/components/icons/bootstrap.svg' }
    ]
  },
  {
    categoria: 'Herramientas y Softwares',
    habilidades: [
      { nombre: 'Git', nivel: 'Intermedio', icono: '/src/components/icons/git.svg' },
      { nombre: 'Docker', nivel: 'Intermedio', icono: '/src/components/icons/docker.svg' },
      { nombre: 'Cypress', nivel: 'Intermedio', icono: '/src/components/icons/cypress.svg' },
      { nombre: 'Visual Studio Code', nivel: 'Avanzado', icono: '/src/components/icons/visual.svg' }
    ]
  },
  {
    categoria: 'Base de Datos',
    habilidades: [
      { nombre: 'MySQL', nivel: 'Intermedio', icono: '/src/components/icons/mysql.svg' },
      { nombre: 'MongoDB', nivel: 'Intermedio', icono: '/src/components/icons/mongo.svg' }
    ]
  },
  {
    categoria: 'Idiomas',
    habilidades: [
      { nombre: 'Español', nivel: 'Nativo', icono: '/src/components/icons/arg.svg' },
      { nombre: 'Inglés', nivel: 'Intermedio', icono: '/src/components/icons/eeuu.svg' }
    ]
  }
];
</script>

<template>
  <div class="skills-contenedor">
    <div v-for="categoria in skillsData" :key="categoria.categoria" class="skills-categoria">
      <h3>{{ categoria.categoria }}</h3>
      <ul class="skills">
        <li v-for="habilidad in categoria.habilidades" :key="habilidad.nombre" class="skill">
          <img :src="habilidad.icono" :alt="habilidad.nombre" />
          <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>


<style scoped>
.skills-contenedor {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  padding: 20px;
  background-color: rgb(28, 41, 52);
  border-radius: 10px;
}

/* Estilo para cada categoría de habilidades */
.skills-categoria h3 {
  font-size: 1.5rem;
  margin-bottom: 15px;
  color: coral;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  position: relative;
}

/* Añadir efecto visual a los títulos */
.skills-categoria h3::after {
  content: "";
  width: 50px;
  height: 3px;
  background-color: #007bff;
  display: block;
  margin: 10px auto;
}

/* Estilo para la lista de habilidades */
.skills {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
}

/* Estilo para cada habilidad individual */
.skill {
  display: flex;
  align-items: center;
  gap: 10px;
  background-color: #fff;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Añadir efecto hover a las habilidades */
.skill:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

/* Estilo para las imágenes dentro de las habilidades */
.skill img {
  width: 40px;
  height: 40px;
  object-fit: cover;
}

/* Estilo para el texto dentro de las habilidades */
.skill span {
  font-size: 1rem;
  color: #333;
  font-weight: 500;
  text-transform: capitalize;
}

/* Añadir efecto hover al texto de las habilidades */
.skill span:hover {
  color: #007bff;
}

/* Media query para pantallas pequeñas */
@media (max-width: 768px) {
  .skills-contenedor {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .skills-categoria {
    width: 100%;
    text-align: center;
  }

  .skills {
    align-items: center;
  }

  .skill {
    justify-content: center;
    width: 100%;
  }
}

</style>