<template>
  <div class="bg-dark">

    <h2 class="text-white">Films</h2>
    <div>
      <FilmsCard v-for="( elem, index ) in propsArrayFilmFiglio" :key="index" :film="elem"/>
    </div>

    <h2 class="text-white">Series</h2>
    <div>
      <SeriesCard v-for="( elem, index ) in propsArraySerieFiglio" :key="index" :film="elem"/>
    </div>

  </div>
</template>

<script>

import FilmsCard from './FilmsCard.vue'
import SeriesCard from './SeriesCard.vue'

export default {
  name: 'FilmList',
  components: {
    FilmsCard,
    SeriesCard
  },
  props: {
    propsArrayFilmFiglio: Array,
    porpsArraySerieFiglio: Array
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
</style>