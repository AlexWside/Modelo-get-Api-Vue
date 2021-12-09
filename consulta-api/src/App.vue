<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
   <!--  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Consulta/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

import Consulta from './components/consulta.vue'

export default {
  name: 'App',
  components: {
    Consulta
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
