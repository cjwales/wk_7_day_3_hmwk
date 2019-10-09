<template lang="html">
  <li>{{country.name}}</li>
</template>

<script>
export default {
  name: 'list-component',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
