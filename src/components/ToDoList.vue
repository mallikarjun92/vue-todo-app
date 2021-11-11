<template>
  <div class="todo">
      <h1>To Do List</h1>
      <div v-bind:key="todo.id" v-for="todo in todo_list">
            <ToDo v-bind:todo="todo"></ToDo>
        </div>
  </div>
</template>

<script>
import ToDo from './ToDo.vue'
export default {
    name: 'ToDoList',
    props: ['todo_list'],
    components: {
      ToDo
    }
}
</script>

<style scoped>
    
</style>