<template>
  <div class="header">
    <h1 class="inline p-2">Boolflix</h1>
    <input 
      type="text" 
      v-model="testoCercato"
      @keydown.enter.prevent="$emit( 'ricerca', testoCercato )"
      placeholder="Cerca un film..."
      class="input"
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
  .inline{
    display: inline-block;
    vertical-align: middle;
    color: #DB0510;
  }

  .input{
    margin-left: 80%;
  }

  .header{
    background-color: rgba(15, 15, 15, 0.973);
  }
</style>