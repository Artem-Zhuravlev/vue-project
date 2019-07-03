<template>
    <div>
        <h2>Pizza name {{ pizzaName }} / {{ reverseName }}</h2>
        <p>Price: {{ pizzaPrice }}</p>
        <button @click="changeName">Change Name</button>
        <button @click="updateCounter">Update counter</button>
    </div>
</template>


<script>
import { eventEmitter } from './main'

export default {
    props: {
        pizzaName: String,
        pizzaPrice: Number
    },

    methods: {
        changeName() {
            this.pizzaName = 'Маргарита';
            this.$emit('nameChanged', this.pizzaName)
        },
        updateCounter() {
            eventEmitter.$emit('counterUpdated')
        }
    },

    computed: {
        reverseName() {
            return this.pizzaName.split('').reverse().join('');
        }
    }
}
</script>
