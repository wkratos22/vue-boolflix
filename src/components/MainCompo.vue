<template>
  <header>
    <!--inserire contenuto componente-->
    <FilmList :propsArrayFilmFiglio="propsArrayFilm" :propsArraySerieFiglio="propsArraySerie"/>
  </header>
</template>

<script>

import FilmList from './partials/FilmList.vue'

export default {
  name: 'MainComp',
  components: {
    FilmList
  },
  props: {
    propsArrayFilm: Array,
    propsArraySerie: Array
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
</style>
