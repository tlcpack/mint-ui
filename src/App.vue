<template>
  <div id="app">
    <Todos v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
    <AddTodo v-on:add-todo="addTodo"/>
  </div>
</template>

<script>
import Todos from './components/Todos';
import AddTodo from './components/AddTodo';

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Attend morning standup',
          completed: false
        },
        {
          id: 2,
          title: 'Send CTO an email',
          completed: false
        },
        {
          id: 3,
          title: 'Unit meeting by 2pm',
          completed: false
        },
        {
          id: 4,
          title: 'Call wifey',
          completed: false
        },
        {
          i: 5,
          title: 'Stop by at the mall',
          completed: false
        }
      ]
    }
  },
  methods: {
    addTodo(newTodoObj) {
      this.todos = [...this.todos, newTodoObj];
    },
    deleteTodo(todoId) {
      this.todos = this.todos.filter(todo => todo.id !== todoId);
    }
  }
}
</script>

