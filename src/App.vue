<template>
  <div id="app">
    <Todos />
  </div>
</template>

<script>
import Todos from './components/Todos';

export default {
  name: 'App',
  components: {
    Todos
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
}
</script>

