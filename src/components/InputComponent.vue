<template>
      <div class="ui input">
        <input type="text" v-on:keyup.enter="inputSave" placeholder="Enter a title for this card...">
      </div>
</template>

<script>
  export default {
    name : 'InputComponent',
    methods : {
      inputSave:function() {
        console.log("엔터엔터")
      }
    }
  }
</script>


