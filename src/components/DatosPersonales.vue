<script setup>
import Linkedin from '/src/assets/linkedin_icon.svg';
import Instagram from '/src/assets/instagram_icon.svg';
import GitHub from '/src/assets/github_icon.svg';
import CurriculumVitae from '/src/assets/cv_resume_icon.svg';
const title = 'José Luis Villalba';
const description1 = 'Licenciado en Seguridad Pública';
const description2 = 'Técnico Universitario en Programación';
const description3 = 'Profesor Universitario';
const residencia = 'Ciudad Autónoma de Buenos Aires, Argentina';
const presentacion = 'Bienvenido a mi Porfolio. Soy un Data Analyst que explora constantemente nuevas formas de ofrecer información procesable y valiosa. Utilizo SQL, Python, IBM i2 Analyst Notebook y herramientas de Inteligencia Empresarial como Power BI, desde los cuales presento mis hallazgos en forma de paneles interactivos fáciles de usar y visualmente agradables';
const redesSociales = [
    { id: 1, name: 'Linkedin', src: Linkedin, url: 'https://www.linkedin.com/in/jose-luis-villalba-03bb29209/' },
    { id: 2, name: 'Instagram', src: Instagram, url: 'https://www.instagram.com/josecho_vba/' },
    { id: 3, name: 'GitHub', src: GitHub, url: 'https://github.com/JosechoVBA' },
    { id: 4, name: 'Curriculum Vitae', src: CurriculumVitae, url: '' }
];
const email = 'joseluisvillalba11@gmail.com';
</script>

<template>
    <section class="datos-personales">
        <div class="card">
            <h1>{{ title }}</h1>
            <h2>{{description1}}</h2>
            <h2>{{description2}}</h2>
            <h2>{{description3}}</h2>
            <p>{{presentacion}}</p>
            <ul class="container-lista">
                <li v-for="red in redesSociales" :key="red.id">
                    <a href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
                </li>
            </ul>
            <h3>✉️ Email: {{email}}</h3>
            <h4>{{ residencia }}</h4>
        </div>
    </section>
</template>

<style scoped>
h1{
    font-size: 2.5rem;
}

p{
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.card {
    background-color: rgb(28, 41, 52);
    border-radius: 10px;
    padding: 10px;
    margin: 10px;
    text-align: center;
}

.container-lista {
    display: flex;
    justify-content: center;
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}

.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
    font-size: 1.2rem;
    font-weight: 600;
}

</style>

