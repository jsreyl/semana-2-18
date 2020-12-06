<template>
    <div class="card">
        <div class="d-flex justify-content-center p-2">
            <div v-if="service.imgurl==1">
                <img src="../assets/servicio1.png" :alt="service.title" class="d-block w-100 mh-100" style="height: 200px">
            </div>
            <div v-else-if="service.imgurl==2">
                <img src="../assets/servicio2.png" :alt="service.title" class="d-block w-100 mh-100" style="height: 200px">
            </div>
            <div v-else>
                <img src="../assets/servicio3.png" :alt="service.title" class="d-block w-100 mh-100" style="height: 200px">
            </div>
        </div>
        <hr>
        <div class="card-body">
            <h5 class="card-title">{{service.title}}</h5>
            <p class="card-text">{{service.descripcion}}</p>
            <div class="d-flex justify-content-center">
                <a :href="service.url" class="btn btn-info justify-content-center">Quiero más información...</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'ServicesCard',
  props:{
      'service': Object,
      'url': String
  }
}
</script>