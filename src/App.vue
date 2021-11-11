<template>
  <div id="app">
    <ToDoList v-bind:todo_list="todo_list" />
    <AddToDo />
  </div>
</template>

<script>
import ToDoList from './components/ToDoList.vue'
import AddToDo from './components/AddToDo.vue'

export default {
  name: 'App',
  components: {
    ToDoList,
    AddToDo
  },

  data() {
    return {
      newToDo: '',
      todo_list : []
    }
  }
}
</script>

<style>
#app {
  color: dimgray;
  text-transform: uppercase;
  align-content: center;
  text-align: center;
}
</style>
