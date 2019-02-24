<template>
  <div class="list">
    <!-- <SpanComponent>dddfkdfkdf</SpanComponent> -->
    <InputComponent></InputComponent>

  </div>
</template>
<script>
  import InputComponent from './InputComponent';
  import SpanComponent from './SpanComponent';
  export default {
    components :{
      InputComponent,
      SpanComponent
    }
  }
</script>
<style>
  .list {
    background-color: #dfe3e6;
    border-radius: 3px;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    max-height: 100%;
    position: relative;
    white-space: normal;
  }
</style>
