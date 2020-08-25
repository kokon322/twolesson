<template>
  <div>
      
     <span>{{item}}</span>

     <button @click="deleteTodo">Delete</button>
     
  </div>
</template>

<script>
export default {
    name: 'TodoItem',
props:{
    item:{
        type: String
    }
},
methods:{
    deleteTodo(){
        this.$emit('deleteTodo',this.item)
    }
}
    
   
}

</script>

<style>

</style>