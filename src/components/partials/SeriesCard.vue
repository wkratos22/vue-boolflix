<template>
  <div class="col-3 row inline p-3">
    <div class="bg-dark p-3 card">
      <h5 class="title">Titolo: {{ serie.title }}</h5>
      <div class="card-text center">
        <span class="text-white">Lingua:</span>
        <!-- <span :class="( film.original_language == 'en') ? 'bandieraen' "></span> -->
      </div>
      <p class="text-white center">Voto: {{ serie.vote_average }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    //Cambiare il nome con quello del componente creato
    name: 'SeriesCard',
    props: {
      serie: Object
    }
  }
</script>

<style scoped lang="scss">


  .title {
    color: white;
    text-align: center;
  }

  .center {
    text-align: center;
  }

  .inline{
    display: inline-block;
    width: calc(30% - 74px)
  }
</style>