<template>
  <div class="list">
    <!-- <SpanComponent>dddfkdfkdf</SpanComponent> -->
    <InputComponent v-on:pushData="updateData($event)"></InputComponent>

    <ul>
      <li v-for="todo in todos" :key="todo.id">
        <div>
        <!-- <input type="checkbox" /> -->
        <label>{{todo.title}}</label>
        <button>삭제</button>
        </div>
      </li>
    </ul>

  </div>
</template>
<script>
  import InputComponent from './InputComponent';
  import SpanComponent from './SpanComponent';
  export default {
    data () {
      return {
        todos : []
      }
    },
    components :{
      InputComponent,
      SpanComponent
    },
    methods : {
      updateData : function(data) {
        console.log(data)





        
        //this.todos.push({title :data, completed:'false', id:this.todos.length});
        //console.log(this.todos)
      }
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
