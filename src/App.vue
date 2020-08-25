<template>
  <div>
  <h1>ToDoList</h1>     
    
  <AddTodo @pushToArray="pushToArray"/>

  <TodoList :arrayTodoList="arrayTodoList"/>

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
    }
  }
}
</script>

<style>

</style>
