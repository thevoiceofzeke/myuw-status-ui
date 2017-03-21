<template>
  <div id="app">
    <app-header></app-header>
    <h2>Apps</h2>
    <!-- FOR EACH (grid of status cards) -->
    <grid-of-cards></grid-of-cards>
  </div>
</template>

<script>
// Get child components
import AppHeader from './components/app-header.vue'
import GridOfCards from './components/grid-of-cards.vue'

export default {
  components: { AppHeader, GridOfCards },
  name: 'app',
  data () {
    return {}
  }
}
</script>

<style lang="scss">
body {
  margin: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  min-width: 300
}

h2 {
  font-weight: normal;
  text-align: center;
  font-size: 2em;
}
</style>
