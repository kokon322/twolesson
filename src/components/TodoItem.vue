<template>
  <div>
      
     <span>{{item}}</span>

     <button>Delete</button>
     
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

    
   
}

</script>

<style>

</style>