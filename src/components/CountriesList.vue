<template lang="html">
  <div>
    <ul>
      <list-component v-for="country in countries" :country="country"></list-component>
    </ul>
  </div>
</template>

<script>
import ListComponent from './ListComponent.vue';
export default {
  name: 'countries-list',
  props: ['countries'],
  components: {
    "list-component": ListComponent
  }
}
</script>

<style lang="css" scoped>
</style>
