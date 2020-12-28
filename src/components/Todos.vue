<template>
  <div>
    <mt-header fixed title="Todo List"></mt-header>
    <mt-index-list :show-indicator=false height=500>
      <mt-index-section v-bind:key="todo.id" v-for="todo in todos">
        <Todo
          v-bind:todo="todo"
          v-on:delete-todo="$emit('delete-todo', todo.id)"
        />
      </mt-index-section>
    </mt-index-list>
  </div>
</template>

<script>
import Todo from "./Todo";

export default {
  name: "Todos",
  components: {
    Todo,
  },
  props: ["todos"],
};
</script>

<style scoped>
</style>