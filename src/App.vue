<template>
  <div id="app">
    <HelloWorld />
    <Charades />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Charades from './components/Charades.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
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
