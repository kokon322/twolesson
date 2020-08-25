<template>
  <div>
  <h1>ToDoList</h1>     
    
  <AddTodo @pushToArray="pushToArray"/>

  <TodoList :arrayTodoList="arrayTodoList"
            @deleteTodo="deleteTodo"
  />

  </div>
</template>

<script>
import AddTodo from "@/components/AddTodo";
import TodoList from "@/components/TodoList"

export default {
  name: 'App',

  components: {
    AddTodo,
    TodoList
  },
  
  data(){
    return{
     arrayTodoList: []
    }
  },
  methods:{
    pushToArray(event){
      this.arrayTodoList.push(event)
      console.log(this.arrayTodoList)
    },
    deleteTodo(event){
      const idx = this.arrayTodoList.findIndex(e => e === event);
      this.arrayTodoList.splice(idx, 1)
    }
  }
}
</script>

<style>

</style>
