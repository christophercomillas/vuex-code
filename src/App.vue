<template>
	<div id="app">
    <h1>Todos</h1>
    <h2>Completed: {{completedTodos}}</h2>
    <h2>Pending: {{pendingTodos}}</h2>
    <TodoList />
    <TodoForm />
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import TodoList from './components/TodoList.vue'
import TodoForm from './components/TodoForm.vue';

export default {
  name: 'App',
  components: {
    TodoList,
    TodoForm
  },
  computed: {
    ...mapGetters({
      completedTodos: "completedTodos",
      pendingTodos: "pendingTodos"
    })
    // completedTodos(){
    //   return this.$store.getters.completedTodos;
    // },
    // pendingTodos(){
    //   return this.$store.getters.pendingTodos;
    // }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
