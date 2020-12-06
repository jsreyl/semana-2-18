<template>
  <div id="app">
    <page-footer></page-footer>
    <h1>{{título}}</h1>
  </div>
</template>

<script>

import PageFooter from './components/PageFooter.vue'

export default {
  name: 'App',
  components:{
    PageFooter
  },
  data(){
    return{
      título : 'Vivo dentro de VUE'
    }
  }
}
</script>

