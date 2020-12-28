<template>
    <div>
        <form @submit="addTodo">
            <mt-field label="To do" placeholder="What do you want to do?" type="textarea" rows="2" v-model="title" name="title"></mt-field>
            <mt-button size="large">Add</mt-button>
        </form>
    </div>
</template>

<script>
import {uuid} from "vue-uuid"; 

export default {
    name: "AddTodo",
    data() {
        return {
            title: ""
        }
    },
    methods: {
        addTodo(e) {
            e.preventDefault();
            const newTodoObj = {
                id: uuid.v4(),
                title: this.title,
            }
            this.$emit("add-todo", newTodoObj);
            this.title = "";
        }
    }    
}
</script>

<style scoped>
</style>