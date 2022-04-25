<template>
  <div>
    <!-- <input v-model="RicercaInput" placeholder="Cerca un film"> -->
    <input
      type="text"
      v-bind:value="film"
      v-on:input="$emit(
        'update:film',
        $event.target.value
      )"
      placeholder="Cerca un film..."
    />
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',

  model: {
    prop: 'film',
    event: 'update:city'
  },

  props: {
    film: {
      type: String,
      default: ''
    }
  }
};
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
</style>