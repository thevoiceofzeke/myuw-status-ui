<template>
  <div id="app">
    <h1>MyUW Status</h1>
    <h2>Apps</h2>
    <!-- FOR EACH (grid of status cards) -->
    <grid-of-cards></grid-of-cards>
  </div>
</template>

<script>
// Get grid component
import GridOfCards from './components/grid-of-cards.vue'

export default {
  components: { GridOfCards },
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
  text-align: center;
}
</style>
