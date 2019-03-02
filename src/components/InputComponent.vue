<template>
      <div class="ui input">
       
        <input type="text" class="toggle"  v-model.trim="newTodo" placeholder="Enter a title for this card...">
        <button v-on:click="addTodo">추가</button>
        <button v-on:click="searchTodo">검색</button>
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
      },
      searchTodo:function(){
        this.$emit('searchData',this.newTodo);
      }
    }
  }
</script>


