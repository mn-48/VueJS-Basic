<template>

</template>


<script setup>
import { onMounted, reactive, ref } from 'vue';


const data = reactive({
  data: []
})

// const OFFICE_API = "https://jsonplaceholder.typicode.com/todos/";
// const OFFICE_API = "https://platform.buildwithhussain/api/method/get-office";
const OFFICE_API = "https://http.cat/wqfver2";

onMounted(() =>{
 fetch('https://jsonplaceholder.typicode.com/todos/')
      .then(response => response.json())
      .then(json => console.log(json))
})
  
</script>