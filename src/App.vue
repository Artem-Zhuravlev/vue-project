<template>
  <div id="app">
    <h1>{{ pizzaName }}</h1>
    <app-pizza :pizzaName="pizzaName" :pizzaPrice="pizzaPrice"></app-pizza>
  </div>
</template>

<script>

import Pizza from './Pizza.vue'

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      pizzaName: 'пицуля',
      pizzaPrice: 180
    }
  },

  components: {
    appPizza: Pizza
  }
}
</script>

<style lang="scss">

</style>
