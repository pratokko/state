<template>
  <div>
    <h1>Todos</h1>
    <h3>completed: {{ completedTodos }}</h3>
    <h3>pending: {{ pendingTodos }}</h3>
    <TodoForm />
    <TodoList />
  </div>
</template>

<script>
import { mapGetters } from 'vuex/dist/vuex.esm-bundler';
import TodoForm from './components/TodoForm.vue';
import TodoList from './components/TodoList.vue';
  export default {
    name:'App',
    components: { TodoList, TodoForm },

    computed: {
      ...mapGetters({
        completedTodos: 'completedTodos',
        pendingTodos: 'pendingTodos'
      })
      
    }
}
</script>