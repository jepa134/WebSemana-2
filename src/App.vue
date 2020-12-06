<template>
  <div id="app">
    <nav-component></nav-component>
    <carousel-component></carousel-component>
    <colombia-news>
      
    </colombia-news>
    <div class="container-fluid">
      <div class="row justifiy-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
        
      </div>
    </div>
    <footer-page></footer-page>
  
  </div>
</template>

<script>


import TeamCard from './components/TeamCard.vue';
import FooterPage from './components/FooterPage.vue';
import NavComponent from './components/NavComponent.vue';
import CarouselComponent from './components/CarouselComponent.vue';
import ColombiaNews from './components/ColombiaNews.vue';



export default {
  name: 'App',
  components: {
    
    TeamCard,
    FooterPage,
    NavComponent,
    CarouselComponent,
    ColombiaNews
    
  },
  data(){
    return{
      team:[
        {
        codigo: 1,
        nombre: "José R. Castillo",
        descripcion: "Ingeniero electrónico egresado de la universidad popular del Cesar",
        rol: "Desarrollador Full-Stack",
        image: "./Perfiljr.jpg"
    },
    {
        codigo: 2,
        nombre: "Jorge Polo", 
        descripcion: "Tecnologo en electónica y comunicaciones egresado de la universidad militar nueva granada" ,
        rol: "Desarrollador Front-End",
        image: "./Jorge.jpg"
    },
    {
        codigo: 3,
        nombre: "Ariaden Gamboa",
        descripcion: "ingeniera de sistemas egresada de la universidad cooperativa de Colombia",
        rol: "Arquitecto de Software",
        image: "./Ariaden.jpg"
    },
    {
        codigo: 4,
        nombre: "Erick Parra",
        descripcion: "Ingeniero industrial egresado de la universidad de la Salle",
        rol: "Scrum Master",
        image: "./Erick.jpg"
    }
    ]
  }
    }
}
</script>
<style scoped>

</style>

