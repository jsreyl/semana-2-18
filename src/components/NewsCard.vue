<template>
    <section id="news">
        <div class="container-fluid">
            <div class="row mt-md-5">
                <!-- Loop through each of the four movies we need -->
                <div class="col-lg-6 col-xs-12" v-for="(item, index) of news" :key="index">
                    <div class="d-flex justify-content-between align-items-center">
                        <div class="p-3">
                            <img :src="item.urlToImage" :alt="item.title" class="d-block w-100">
                        </div>
                        <div class="p-2">
                                <h4>{{ item.title }}</h4>
                                <hr>
                                <p>{{item.description}}</p>
                        </div>
                    </div>
                    <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                        <button type="button" class="btn btn-outline-info"><a :href="item.url" target="_blank" rel="noopener noreferrer">Leer más</a></button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import axios from "axios";

export default {
  name: 'NewsCard',
  data(){
      return{
          //Array to store news, we need 4
          news:null
      }
  },
  mounted(){
      //Use axios to get news from the API
      axios
      .get('https://newsapi.org/v2/top-headlines?country=co&category=technology&apiKey=f17b2dcef15f4dc68cb959519bd71c55')
      .then(response =>{
          (this.news=response.data.articles.slice(0,4)); //Slice since we only need 4 news to display
          console.log(this.news)
      })
  }
}
</script>