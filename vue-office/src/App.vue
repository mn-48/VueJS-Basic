<template>

</template>


<script setup>

const OFFICE_API = "https://school.frappe.io/api/method/get-office/";
// const OFFICE_API = "https://platform.buildwithhussain/api/method/get-office";

fetch(OFFICE_API)
.then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error('Error fetching office data:', error);
  });

</script>

  