<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <translateIn></translateIn>
    <h1>Traductor</h1>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import translateIn from './components/translateIn'

export default {
  name: 'app',
  components: {
    translateIn
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
