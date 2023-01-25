<template>
  <div>
    <span :class="{ completed: todo.completed }" @click="toggleTodoStatus(todo)">
      {{ todo.title }}
    </span>
    <button @click="deleteTodo(todo)">X</button>
  </div>
</template>

<script>
import { mapActions } from 'vuex/dist/vuex.esm-bundler';
    export default {
        props:['todo'],
        methods : {
            ...mapActions({

         deleteTodo: 'deleteTodo',
                toggleTodoStatus: 'toggleTodoStatus'
            })
           
        }

    }
</script>
<style scoped>
.completed {
  text-decoration: line-through;
}
</style>
