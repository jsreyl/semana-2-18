<template>
    <div class="card">
        <div class="d-flex justify-content-center p-2">
            <img :src="service.image" :alt="service.title" class="d-block mh-100" style="height: 200px">
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
      'service': Object
    }
}
</script>