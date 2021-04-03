<template>
  <div id="app">
    <ListaTodo msg="Crear una nueva tarea"/>
  </div>
</template>

<script>
import ListaTodo from './components/ListaTodo.vue'

export default {
  name: 'App',
  components: {
    ListaTodo
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
