<template>
  <div class="container-fluid">
    <div class="row mt-md-5 mt-sm-5 mt-xs-5" >
      <div class="col-lg-6 col-xs-12 " v-for="(item, index) of news.data.articles" :key="index">
        <div class="d-flex justify-content-center align-items-center" >
          <div class="p-3">
              <img :src="news.data.articles[index].urlToImage" alt="imagen" width="200px">
            
          </div>

          <div class="p-2">
            <h3>{{news.data.articles[index].title}}</h3>
            <p>
              {{news.data.articles[index].description}}
            </p>
          </div>
        </div>
        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
          <a v-bind:href="news.data.articles[index].url" target="blank" type="button" class="btn btn-outline-info">Ver Mas</a>
        </div>
      </div>

    </div>
    
  </div>
  
</template>

<script>
import axios from "axios";
export default {
  name: "ColombiaNews",
  data() {
    return {
      news: null,
    };
  },
  mounted() {
    axios
      .get(
        "http://newsapi.org/v2/top-headlines?country=co&pageSize=4&apiKey=a4c45a323faf4baa8a12cbc4bda93593"
      )
      .then((response) => (this.news = response));
  },
};
</script>

<style lang="stylus" scoped></style>
