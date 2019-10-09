<template lang="html">
  <div>
    <h1>Countries</h1>
    <countries-list :countries='countries'></countries-list>
    <country-detail :country='selectedCountry'></country-detail>
  </div>
</template>

<script>
import {eventBus} from './main.js';
import CountriesList from './components/CountriesList.vue';
import ListComponent from './components/ListComponent.vue';
import CountryDetail from './components/CountryDetail';

export default {
  name: 'app',
  data(){
    return {
      countries: [],
      selectedCountry: null
    }
  },
  mounted(){
    fetch('https://restcountries.eu/rest/v2/all')
    .then(res => res.json())
    .then(countries => this.countries = countries)

    eventBus.$on('selected-country', (country) => {
      this.selectedCountry = country;
    })
  },
  components: {
    "countries-list": CountriesList,
    "list-component": ListComponent,
    "country-detail": CountryDetail
  }
}
</script>

<style lang="css" scoped>
</style>
