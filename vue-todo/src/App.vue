<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" placeholder="Add a description" v-model="data.todoDescriptions" />
      <button type="submit">Add</button>

    </form>
    <ol>

      <li v-for="(todo, index) in data.todos" :key="index">
        <del v-if="todo.completed">{{ todo.description }}</del>
        <span v-else>{{ todo.description }}</span>
        <button @click="deleteTodo(index)">
          Delete 
          <i class="trash icon"> 🗑️</i>
        </button>
        <button @click="completeTodo(index) " :hidden="todo.completed">
          Complete 
          <i class="check icon"> ✅</i>
        </button>
        <!-- <button @click="completeTodo(index) " :disabled="todo.completed">
          Complete 
          <i class="check icon"> ✅</i>
        </button> -->
      </li>
    </ol>

  </div>

</template>

<script setup>
import { reactive } from 'vue'

const data = reactive({
  todos: [],
  todoDescriptions: ""
})  





const addTodo = () => {
  if (data.todoDescriptions.trim()) {

    console.log('New Todo:', data.todoDescriptions);
    data.todos.push({
      description: data.todoDescriptions,
      completed: false
    });
    data.todoDescriptions = '';
  }
}

const deleteTodo = (index) => {
  data.todos.splice(index, 1);
}

const completeTodo = (index) => {
  data.todos[index].completed = true;
} 




</script>