<template lang="html">
  <div v-if="country">
    <h3>{{country.name}}</h3>
    <p>Capital: {{country.capital}}</p>
    <p>Population: {{country.population}}</p>
    <img :src="country.flag">
  </div>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
div {
  border: 2px solid black;
  max-height: 260px;
  background-color: silver;
}
img {
  max-width: 200px;
}
</style>
