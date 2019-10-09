<template lang="html">
  <li v-on:click="handleClick">{{country.name}}</li>
</template>

<script>
import {eventBus} from '../main.js'
export default {
  name: 'list-component',
  props: ['country'],
  methods: {
    handleClick() {
      eventBus.$emit('selected-country', this.country)
      // console.log("hello");
    }
  }
}
</script>

<style lang="css" scoped>
</style>
