<template>
  <div>
 <city-Header></city-Header>
  <city-Search></city-Search>
  <city-list></city-list>
  <city-Alphabet></city-Alphabet>
  </div>
</template>
<script>
  import CityHeader from './components/Header'
  import CitySearch from './components/Search'
  import CityList from './components/List'
  import CityAlphabet from './components/Alphabet'
  export default {
    name: 'city',
    components: {
      CityHeader,
      CitySearch,
      CityList,
      CityAlphabet
    }
  }

</script>
<style lang="stylus" scoped>


</style>
