<template>

  <div id="app">
    <app-header></app-header>
    <Canvas></Canvas>
    <InputComponent></InputComponent>
    <!--<router-view/>-->
  </div>
</template>

<script>
  import InputComponent from "./components/Input";

export default {
  name: 'App',
  components: {
    InputComponent,

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
