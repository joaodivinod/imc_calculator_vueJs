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
    display: flex;
}
@media(max-width: 600px){
    #app{
        width: 100%;
        height: 100vh;
    }
}
</style>
