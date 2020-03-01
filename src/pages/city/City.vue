<template>
    <div>
      <city-header></city-header>
      <city-search></city-search>
    </div>
</template>

<script>
import CityHeader from './componentes/Header.vue'
import CitySearch from './componentes/Search.vue'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch
  }
}
</script>

<style lang="stylus" scoped>
</style>
