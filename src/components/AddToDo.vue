<template>
    <div>
        <form @submit="addToDo">
            <input type="text" v-model="title" name="title" placeholder="Add Todo item...">
            <input type="submit" value="Submit" class="btn">
        </form>
    </div>
</template>

<script>
import uuid from 'uuid/v4'
export default {
    name: 'AddToDo',
    data() {
        return {
            title: ''
        }
    },

    methoods: {
        addToDo(e) {
            e.preventDefault();
            const newToDo = {
                title: this.title,
                id: uuid()
            }

            this.$emit('add-todo-event', newToDo);
            this.title = ''
        }
    }
}
</script>

<style>

</style>