<template lang="html">
  <li v-on:click="handleClick">{{country.name}}</li>
</template>

<script>
import { eventBus } from '../main.js'
export default {
    name: 'list-component',
    props: ['country'],
    methods: {
        handleClick: function() {
            eventBus.$emit('selected-country', this.country);
        }
    }
}
</script>

<style lang="css" scoped>
</style>