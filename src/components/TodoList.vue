<template>
  <div>
<Todo  v-for="(todo, index) in todos" :key="index" :todo="todo"/>
  </div>
</template>

<script>
import { mapState } from 'vuex/dist/vuex.esm-bundler';
import Todo from './Todo.vue';
export default {
    components: {Todo},

    computed : { 
        ...mapState ({
            todos: 'todos'
        })
    }
};
</script>
