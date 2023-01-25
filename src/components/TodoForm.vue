<template>
  <div>
    <input type="text" v-model="newTodoItem">
    <button @click="addTodo">add todo</button>
  </div>
</template>

<script>
export default {
    data(){
        return {
            newTodoItem: ''
        }
    },

    methods : {
        addTodo(){

            if(this.$store) {
   this.$store.dispatch('addNewTodo', this.newTodoItem)
}
        }
    }
};
</script>
