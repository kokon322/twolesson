<template>
  <div>
      
      <input v-model="inputScan" type="text">
      <button @click="saveToArrey">Add</button>
      
     
  </div>
</template>

<script>

export default {
    name: 'AddTodo',
    data(){
        return{
        inputScan:'',
        }
    },
    
    methods:{
        saveToArrey(){
            this.$emit('pushToArray', this.inputScan)
            this.inputScan = ''
        }
    }
}


</script>

<style>

</style>