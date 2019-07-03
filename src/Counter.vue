<template>
    <h2>Счетчик {{ counter }}</h2>
</template>

<script>

import {eventEmitter} from './main'

export default {
    data() {
        return{
            counter: 0
        }
    },

    created() {
        eventEmitter.$on('counterUpdated', ()=>{
            this.counter++
        })
    }
}
</script>

