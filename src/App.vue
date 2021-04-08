<template>
  <div id="app">
      <Imc></Imc>
  </div>
</template>

<script>
require('@/assets/css/main.css')
import Imc from './components/imc'
export default {
  name: 'App',
  components: {
      Imc
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
