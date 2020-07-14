<template>
  <div id="app">
    <div class="jumbotron mt-3">
      <h1>Parcial</h1>
      <Padre/>
    </div>
  </div>
</template>

<script>
import Padre from './components/Padre.vue'

export default {
  name: 'App',
  components: {
    Padre
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
