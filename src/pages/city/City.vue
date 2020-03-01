<template>
    <div>
      <city-header></city-header>
      <city-search></city-search>
      <city-list></city-list>
      <city-alphabet></city-alphabet>
    </div>
</template>

<script>
import CityHeader from './componentes/Header.vue'
import CitySearch from './componentes/Search.vue'
import CityList from './componentes/list.vue'
import CityAlphabet from './componentes/Alphabet.vue'
export default {
  name: 'City',
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
