<template>
    <div>
        <p>
            <span :class="{completed: todo.completed}" @click="toggleTodoStatus(todo)">{{ todo.title }}</span> 
             <button @click="deleteTodo(todo)">Delete</button>
        </p>
    </div>    
</template>

<script>
import { mapActions } from "vuex";
export default {
    props: ["todo"],
    methods:{
        ...mapActions({
            deleteTodo:"deleteTodo",
            toggleTodoStatus:"toggleTodoStatus"
        })
        // deleteTodo () {
        //     this.$store.dispatch('deleteTodo', this.todo);
        // },
        // toggleTodoStatus() {
        //     this.$store.dispatch('toggleTodoStatus', this.todo);
        // }
    }
}
</script>

<style>
.completed {
    text-decoration: line-through;
}
</style>