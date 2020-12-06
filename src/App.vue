<template>
  <div id="app">
    <div id="news" class="container-fluid">
      <section-api></section-api>
    </div>
  <div id="team" class="container-fluid">
  <div class="row justify-content-center mb-4">
    <div class="col mt-4" v-for="(item, index) of team" :key="index">

  <team-card v-bind:member="item"></team-card>
  
    </div>
  </div>
 </div>

    <page-footer></page-footer>,

  
  </div>
</template>

<script>
import PageFooter from './components/PageFooter.vue';
import TeamCard from './components/TeamCard.vue';
import SectionApi from "./components/SectionApi.vue";



export default {
  name: 'App',
  components:{
    PageFooter,
    TeamCard,
    SectionApi,
    
  },
  data(){
    return{
      team: [
        {
          codigo: 1018488346,
          nombre: "Paul Roldán Olarte",
          descripcion: 'Bioingeniero de 24 años de edad. Apasionado de la biotecnología y la ingeniería aplicada a proyectos relacionados con el campo de la agricultura, la biodiversidad y la sostenibilidad. Amante de la natación con aletas y el deporte en general. Actualmente trabaja en un proyecto de emprendimiento para produccion de peces nativos del a región amazonica en un sistema acuapónico.',
          rol: 'Desarrollador Sección Equipo',
          image: 'imagenes/fotoPaul.jpeg',
        }, 
        {
          codigo: 1015457400,
          nombre: "Juan Sebastian Riaño",
          descripcion: 'Juan Sebastián Riaño Patiño , 25 años Administrador deportivo en formación , amante del futbol , el ciclismo y las artes audiovisuales , interesado en el desarrollo de software enfocado tanto para la gerencia de entidades deportivas , como para la gestión y análisis de disciplinas deportivas , actualmente trabaja en un proyecto de emprendimiento para la creación de un servicio de cardio Tennis en la ciudad de Bogotá.',
          image: 'imagenes/fotoSebastian.jpeg',
          rol: 'Desarrollador Sección Servicios' 
        }, 
        {
          codigo: 1070924825,
          nombre: "Cristian Ferney",
          descripcion: 'Cristian Alvarez, Lic Fisica y estudiante de maestria, enamorado de la ciencia la musica y la comida , interesado en enseñanza atraves de la programación.',
          image: 'imagenes/cristian.JPG',
          rol: "Desarrollador Sección Noticias",
        }, 
        {
          codigo: 1023923186,
          nombre: "Alejandro Bermúdez",
          descripcion: 'Luis Alejandro Bermúdez Valdés, 24 años Ingeniero mecánico egresado de la Universidad Nacional de Colombia, me gusta hacer ejercicio, practica running y futbol, interesado en la programación, uso eficiente de la energía, energías renovables y automatización industrial',
          image: 'imagenes/alejandro.JPG',
          rol: "Desarrollador Sección Header y Footer",
        }, 
      ]
    }
  }
}
</script>

<style scoped>

</style>

