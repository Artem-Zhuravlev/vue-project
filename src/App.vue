<template>
  <div id="app">
    <h1>{{ pizzaName }}</h1>
    <app-pizza 
      :pizzaName="pizzaName" 
      :pizzaPrice="pizzaPrice"
      @nameChanged="pizzaName = $event"
      @counterUpdated="counter = $event"
    ></app-pizza>

    <app-counter>

    </app-counter>
  </div>
</template>

<script>

import Pizza from './Pizza.vue'
import Counter from './Counter.vue'

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
    appPizza: Pizza,
    appCounter: Counter
  }
}
</script>

<style lang="scss">

</style>
