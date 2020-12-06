<template>
  <div id="app">
    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col-md-4 mt-5" v-for="(item, index) of equipo" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>
    <page-footer></page-footer>
    <h1>{{título}}</h1>
  </div>
</template>

<script>

import PageFooter from './components/PageFooter.vue'
import TeamCard from './components/TeamCard.vue'

export default {
  name: 'App',
  components:{
    PageFooter,
    TeamCard
  },
  data(){
    return{
      equipo: [
        {
          codigo: 1,
          nombre: "Alejandro Díaz Moscoso",
          descripcion: "Vive en Armenia, Quindío. Este joven de 27 años es químico de la Universidad del Quindío, y Magíster en Ciencias-Química de la Universidad de los Andes. Entre sus pasatiempos están: Mirar series/películas (ahora con el curso MisiónTIC2022 ni tiempo tiene); hacer cursos virtuales (MisiónTIC2022, Cambio Climático y Huella de Carbono, Diplomado en Excel que consta de 4 cursos, y dos idiomas); ir a cine; salir a tomar café (solo o con amigos); comer ensalada de frutas; y de vez en cuando salir a rumbear. No le gusta tomar. Actualmente está criando un polluelo llamado Duke",
          rol: "Arquitecto de Software",
          image: require("./imagenes/alejo.jpg"),
        },
        {
          codigo: 2,
          nombre: "Juan Sebastián Rey Lancheros",
          descripcion: "Vive en Bogotá D.C. Este joven de 22 años es físico de la Universidad Nacional de Colombia. Entre sus pasatiempos están: Leer (de todo un poco porque gusta de variar géneros, pero sus favoritos son los libros de fantasía, tipo 'El señor de los anillos'); bailar; y jugar videojuegos (¿y a quién no?). Aunque parezca tímido, es un muchacho tranquilo y muy empático. Su mascota es una linda perrita llamada Totó.",
          rol: "Desarrollador Fullstack",
          image: require("./imagenes/juan.jpg"),
        },
        {
          codigo: 3,
          nombre: "Martha Isabel Betancourt Castañeda",
          descripcion: "Vive en Popayán, Cauca. Esta joven es ingeniera de sistemas de la Corporación universitaria Remington. Entre sus pasatiempos están: Estudiar y aprender. Es una persona activa, trabajadora y siempre le pone la mejor actitud a cada situación que se le presenta. Actualmente trabaja de noche por lo que valora mucho la oportunidad de estudiar en el día.",
          rol: "Analista de software",
          image: require("./imagenes/martha.jpg"),
        },
      ],
    }
  }
}
</script>

