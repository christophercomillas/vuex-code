<template>
  <div>
      <input type="text" v-model="newTodoItem" ref="add"/> 
      <button @click="addNewTodoItem()">Submit</button>

  </div>
</template>

<script>
export default {
    data(){
        return {
            newTodoItem: ""
        };
    },
    methods: {
        addNewTodoItem() {
            this.$store.dispatch('addNewTodo', this.newTodoItem);
            this.newTodoItem = "";
            this.$refs.add.focus();
        }
    }
}
</script>

<style>

</style>