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
margin: auto;
}
</style>
