<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import axios from 'axios'

  export default {
    name: 'App',
    components: {
      HelloWorld
    },
    data(){
      return{
        ArrayFilm: []
      }
      
    },
    created() {
    axios.get('https://api.themoviedb.org/3/search/movie?api_key=d542398f5a6299c783607744da728d32&query= ${RicercaInput} &region=IT')
      .then((res) => {
        console.log(res.data);
        this.ArrayFilm = res.data
      })
      .catch((error) => {
        console.log(error)
      })
  }
  }
</script>

<style lang="scss">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>