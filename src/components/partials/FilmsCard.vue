<template>
  <div class="col-3 row inline p-3">
    <div class="bg-dark p-3 card"
    :style="{ backgroundImage: `url ( https://image.tmdb.org/t/p/w342/${film.poster_path} )`}">
      <h5 class="title">Titolo: {{ film.title }}</h5>
      <div class="card-text center">
        <span class="text-white flex">Lingua:</span>
        <span :class="( film.original_language == 'en') ? 'bandieraEN' : ( film.original_language == 'it' ) ? 'bandieraIT' : 'bandieraNO' "></span>
      </div>
      <p class="text-white center">Voto: {{ film.vote_average }}</p>
    </div>
  </div>

</template>

<script>
  export default {
    //Cambiare il nome con quello del componente creato
    name: 'FilmsCard',
    props: {
      film: Object
    }
  }
</script>

<style scoped lang="scss">


  .bandiera-EN{
    background-image: url('../../assets/icons8-great-britain-48.png');
  }

  .bandiera-IT{
    background-image: url('../../assets/icons8-italy-48.png');
  }

  .bandiera-NO{
    background-image: url('../../assets/icons8-punto-interrogativo-50.png');
  }

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