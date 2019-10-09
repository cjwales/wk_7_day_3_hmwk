<template lang="html">
  <div>
    <h1>Countries</h1>
    <ul>
      <li v-for="country in countries">{{country.name}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      countries: [],
    }
  },
  mounted(){
    fetch('https://restcountries.eu/rest/v2/all')
    .then(res => res.json())
    .then(countries => this.countries = countries)
  }
}
</script>

<style lang="css" scoped>
</style>
