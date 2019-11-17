<template>
  <div id="app">
    <recipes-view></recipes-view>
  </div>
</template>

<script>
import RecipesView from './components/RecipesViewComponent.vue'

export default {
  name: 'app',
  components: {
    RecipesView
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
