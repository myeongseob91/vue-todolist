<template>
  <div class="list">
    <!-- <SpanComponent>dddfkdfkdf</SpanComponent> -->
    <InputComponent v-on:pushData="updateData($event)" v-on:searchData="searchData($event)"></InputComponent>

    <ul>
      <li v-for="(todo,index) in todos" :key="todo.id">
        <div>
        <!-- <input type="checkbox" /> -->
        <label>{{todo.title}}</label>
        
        <button v-on:click="removeTodo">삭제</button>
        <button v-if="todo.completed" @click="compelete(index)" class="complete completed">Complete</button>
        <button v-else @click="compelete(index)" class="complete">Complete</button>
        </div>
      </li>
    </ul>

  </div>
</template>
<script>
  import InputComponent from './InputComponent';
  import SpanComponent from './SpanComponent';
  const STORAGE_KEY = 'todo-storage';
  export default {
    data () {
      return {
        todos : [],
        search : ""
      }
    },
    created() {
      this.todos = JSON.parse(localStorage.getItem(STORAGE_KEY) || '[]');
    },
    computed: {
      filterList() {
        return list.filter(item => item.title === this.search);
      }
    },
    components :{
      InputComponent,
      SpanComponent
    },
    methods : {
      updateData : function(data) {
        this.todos.push({title :data, completed:'false', id:this.todos.length});
        localStorage.setItem(STORAGE_KEY, JSON.stringify(this.todos))
      },
      removeTodo : function(todo) {
        this.todos.splice(this.todos.indexOf(todo),1);
        localStorage.setItem(STORAGE_KEY, JSON.stringify(this.todos))
      },
      compelete : function(index) {
        this.todos[index].completed = !this.todos[index].completed;
      },
      searchData : function(data) {
        console.log(this.todos)

        this.todos.filter(function (item) {
           console.log(item.title.match(data));
        })
      }
    }
  }
</script>
<style>
        button {
            color: #ffffff;
        }
        button.complete {
            background-color: #b2b2b2;
        }
        button.complete.completed {
            background-color: #5ddf0f;
        }

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
