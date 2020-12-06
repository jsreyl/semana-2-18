<template>
  <div id="app">
    <PageHeader></PageHeader>
    <PageBanner></PageBanner>
    <section id="services">
      <div class="container-fluid">
        <div class="row justify-content-center mb-5">
            <div class="col-sm-6 col-xs-12 col-lg-4 mt-5" v-for="(sv,index) of services" :key="index">
              <ServicesCard v-bind:service="sv"></ServicesCard>
            </div>
        </div>
      </div>
    </section>
    <NewsCard></NewsCard>
    <section id="team">
      <div class="container-fluid">
        <div class="row justify-content-center mb-5">
          <div class="col-md-4 mt-5" v-for="(item, index) of equipo" :key="index">
            <team-card v-bind:member="item"></team-card>
          </div>
        </div>
      </div>
    </section>
    <page-footer></page-footer>
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue';
import PageBanner from './components/PageBanner.vue';
import ServicesCard from './components/ServicesCard.vue';
import NewsCard from './components/NewsCard.vue';
import TeamCard from './components/TeamCard.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'App',
  components:{
    PageHeader,
    PageBanner,
    ServicesCard,
    NewsCard,
    TeamCard,
    PageFooter
  },
  data(){
    return{
      services: [
        {
          title:"Arquitectura de Servicios Tecnológicos",
          descripcion:"Busca apoyar a la Dirección de Tecnologías y Sistemas de la Información o a quien haga sus veces con lineamientos y estándares orientados a la definición y diseño de la Arquitectura de la infraestructura tecnológica que se requiere para soportar los Sistemas de Información y el portafolio de servicios.",
          url:"https://www.mintic.gov.co/arquitecturati/630/w3-propertyvalue-8095.html",
          image: require("./assets/servicio1.png")
        },
        {
          title:"Operación de Servicios Tecnológicos",
          descripcion:"Busca estructurar e implementar los procesos de operación, monitoreo y supervisión de los Servicios Tecnológicos.",
          url:"https://www.mintic.gov.co/arquitecturati/630/w3-propertyvalue-8096.html",
          image: require("./assets/servicio2.png")
        },
        {
          title:"Gestión de la calidad y seguridad de los Servicios Tecnológicos",
          descripcion:"Busca la definición y gestión de los controles y mecanismos para alcanzar los niveles requeridos de seguridad y trazabilidad de los Servicios Tecnológicos.",
          url:"https://www.mintic.gov.co/arquitecturati/630/w3-propertyvalue-8098.html",
          image: require("./assets/servicio3.png")}
      ],
      equipo: [
        {
          codigo: 1,
          nombre: "Alejandro Díaz Moscoso",
          descripcion: "Vive en Armenia, Quindío. Este joven de 27 años es químico de la Universidad del Quindío, y Magíster en Ciencias-Química de la Universidad de los Andes. Entre sus pasatiempos están: Mirar series/películas (ahora con el curso MisiónTIC2022 ni tiempo tiene); hacer cursos virtuales (MisiónTIC2022, Cambio Climático y Huella de Carbono, Diplomado en Excel que consta de 4 cursos, y dos idiomas); ir a cine; salir a tomar café (solo o con amigos); comer ensalada de frutas; y de vez en cuando salir a rumbear. No le gusta tomar. Actualmente está criando un polluelo llamado Duke",
          rol: "Arquitecto de Software",
          image: require("./assets/alejo.jpg")
        },
        {
          codigo: 2,
          nombre: "Juan Sebastián Rey Lancheros",
          descripcion: "Vive en Bogotá D.C. Este joven de 22 años es físico de la Universidad Nacional de Colombia. Entre sus pasatiempos están: Leer (de todo un poco porque gusta de variar géneros, pero sus favoritos son los libros de fantasía, tipo 'El señor de los anillos'); bailar; y jugar videojuegos (¿y a quién no?). Aunque parezca tímido, es un muchacho tranquilo y muy empático. Su mascota es una linda perrita llamada Totó.",
          rol: "Desarrollador Fullstack",
          image: require("./assets/juan.jpg")
        },
        {
          codigo: 3,
          nombre: "Martha Isabel Betancourt Castañeda",
          descripcion: "Vive en Popayán, Cauca. Esta joven es ingeniera de sistemas de la Corporación universitaria Remington. Entre sus pasatiempos están: Estudiar y aprender. Es una persona activa, trabajadora y siempre le pone la mejor actitud a cada situación que se le presenta. Actualmente trabaja de noche por lo que valora mucho la oportunidad de estudiar en el día.",
          rol: "Analista de Software",
          image: require("./assets/martha.jpg")
        },
      ]
    }
  }
}
</script>

