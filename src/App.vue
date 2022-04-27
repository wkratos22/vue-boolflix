<template>
  <div id="app">

    <HeaderComp @ricerca="funRicercaFilm" />

    <MainCompo :propsArrayFilm="ArrayFilm" :propsArraySerie="ArraySerie" />

  </div>
</template>

<script>
  import MainCompo from './components/MainCompo.vue'
  import HeaderComp from './components/HeaderComp.vue'
  import "bootstrap"
  import axios from 'axios'

  export default {
    name: 'App',

    components: {
      HeaderComp,
      MainCompo

    },
    data() {
      return {
        ArraySerie: [],
        ArrayFilm: [],
        apiKey: 'd542398f5a6299c783607744da728d32',
      }
    },
    methods: {
      funRicercaFilm(testoCercato) {
        axios.get(`https://api.themoviedb.org/3/search/movie?api_key=${this.apiKey}&query= ${testoCercato} &region=IT`)
          .then((res) => {
            console.log(testoCercato);
            console.log(res.data.results);
            this.ArrayFilm = res.data.results
          })

          axios.get(`https://api.themoviedb.org/3/search/movie?api_key=${this.apiKey}&query= ${testoCercato} &region=IT`)
          .then((res) => {
            console.log(testoCercato);
            this.ArraySerie = res.data.results
            })
      },
    }
  }
</script>

<style lang="scss">
  @import "bootstrap/dist/css/bootstrap.min.css";
</style>