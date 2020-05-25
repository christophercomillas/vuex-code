<template>
  <div>
      <Todo v-for="(todo, index) in todos" :key="index" :todo="todo"/>
  </div>
</template>

<script>
import { mapState } from "vuex";
import Todo from "./Todo.vue";
export default {
    components:{
        Todo
    },
    computed: {
        ...mapState({
            todos: 'todos'
        })
    }
}
</script>

<style>

</style>

<!--https://www.youtube.com/watch?v=FIL0za5MzZA -->
<!-- https://www.youtube.com/watch?v=JDR7_AHk9D4&list=PL1TrjkMQ8UbVSDkDaLkjpeNGkblNU8rpW&index=2 -->
