<template>

  <div id="app">
    <app-header></app-header>
    <Canvas></Canvas>
    <!--<router-view/>-->
  </div>
</template>

<script>
  import Canvas from "./components/Canvas";

export default {
  name: 'App',
  components: {
    Canvas,

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
