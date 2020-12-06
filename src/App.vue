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
  </div>
</template>

<script>
import NewsCard from './components/NewsCard.vue';
import PageHeader from './components/PageHeader.vue';
import PageBanner from './components/PageBanner.vue';
import ServicesCard from './components/ServicesCard.vue';

export default {
  name: 'App',
  components:{
    PageHeader,
    PageBanner,
    ServicesCard,
    NewsCard
  },
  data(){
    return{
      services: [
        {
          title:"Arquitectura de Servicios Tecnológicos",
          descripcion:"Busca apoyar a la Dirección de Tecnologías y Sistemas de la Información o a quien haga sus veces con lineamientos y estándares orientados a la definición y diseño de la Arquitectura de la infraestructura tecnológica que se requiere para soportar los Sistemas de Información y el portafolio de servicios.",
          url:"https://www.mintic.gov.co/arquitecturati/630/w3-propertyvalue-8095.html",
          imgurl: 1
        },
        {
          title:"Operación de Servicios Tecnológicos",
          descripcion:"Busca estructurar e implementar los procesos de operación, monitoreo y supervisión de los Servicios Tecnológicos.",
          url:"https://www.mintic.gov.co/arquitecturati/630/w3-propertyvalue-8096.html",
          imgurl:2
        },
        {
          title:"Gestión de la calidad y seguridad de los Servicios Tecnológicos",
          descripcion:"Busca la definición y gestión de los controles y mecanismos para alcanzar los niveles requeridos de seguridad y trazabilidad de los Servicios Tecnológicos.",
          url:"https://www.mintic.gov.co/arquitecturati/630/w3-propertyvalue-8098.html",
          imgurl:3
        }
      ]
    }
  }
}
</script>

