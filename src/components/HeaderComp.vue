<template>
  <div>
    <!-- <input v-model="RicercaInput" placeholder="Cerca un film"> -->
    <input 
      type="text" 
      v-model="testoCercato"
      @keydown.enter.prevent="$emit( 'ricerca', testoCercato )"
      placeholder="Cerca un film..."
    />
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',

  data(){
    return{
    testoCercato: '',
    }  
  },
};
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
</style>