<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <HeaderComp @ricerca="funRicercaFilm" />

    <MainCompo/>

  </div>
</template>

<script>
  import MainCompo from './components/MainCompo.vue'
  import HeaderComp from './components/HeaderComp.vue'
  import axios from 'axios'

  export default {
    name: 'App',

    components: {
      HeaderComp,
      MainCompo

    },
    data() {
      return {
        ArrayFilm: [],
        apiKey: 'd542398f5a6299c783607744da728d32',
      }
    },

    methods: {
      funRicercaFilm(testoCercato) {
        axios.get('https://api.themoviedb.org/3/search/movie?api_key=${this.apiKey}&query=${tetoCercatos}')
          .then((res) => {
            console.log(testoCercato);
            console.log(res.data.results);
            this.ArrayFilm = res.data.results
          })
      },
    }
  }
</script>

<style lang="scss">
  
</style>