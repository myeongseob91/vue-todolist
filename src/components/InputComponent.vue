<template>
      <div class="ui input">
       
        <input type="text" class="toggle" v-on:keyup.13.prevent="addTodo" v-model.trim="newTodo" placeholder="Enter a title for this card...">
      </div>
</template>

<script>
  export default {
    name : 'InputComponent',
    data() {
      return {
        newTodo :''
      }
    },
    methods : {
      addTodo:function() {
        this.$emit('pushData',this.newTodo);
       this.newTodo = '';
      }
    }
  }
</script>


