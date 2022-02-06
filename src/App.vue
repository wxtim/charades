<template>
  <div id="app">
    <h1>Tim's Charades Games</h1>
    <Menu />
    <Charades />
  </div>
</template>

<script>
import Charades from './components/Charades.vue'
import Menu from './components/Menu.vue'

export default {
  name: 'App',
  components: {
    Menu,
    Charades
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
