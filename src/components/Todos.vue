<template>
    <div>
        <mt-header fixed title="Todo List"></mt-header>
        <mt-index-section v-bind:key="todo.id" v-for="todo in todos">
            <Todo v-bind:todo="todo"/>
        </mt-index-section>
    </div>
</template>

<script>
import Todo from './Todo';

export default {
    name: "Todos",
    components: {
        Todo
    },
    props: ["todos"]
}
</script>

<style scoped>
</style>