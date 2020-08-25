<template>
  <div>
      <div 
      v-for="(item, i) in arrayTodoList" 
      :key="i"
      >
           
     <TodoItem :item="item"
                  
/>

  </div></div>
</template>

<script>
import TodoItem from "@/components/TodoItem"

export default {
    name: 'TodoList',

    props:{
        arrayTodoList:{
            type: Array
        }
    },

    components: {
        TodoItem
    },
   
    }

   

</script>

<style>

</style>