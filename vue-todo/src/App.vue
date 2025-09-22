<template>
  <div>

    <form @submit.prevent="addTodo">
      <input type="text" placeholder="Add a todo" v-model="newTodo" />
      <button type="submit">Add</button>
    </form>
  </div>

</template>

<script setup>
import { ref } from 'vue'

const newTodo = ref('')

const addTodo = () => {
  if (newTodo.value.trim()) {
    // Emit the new todo item
    // emit('add-todo', newTodo.value)
    console.log('New Todo:', newTodo.value)
    newTodo.value = ''
  }
}

</script>