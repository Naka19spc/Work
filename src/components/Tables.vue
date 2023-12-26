<script setup>

const props = defineProps(['listUsers'])
console.log("listuser123", props.listUsers);

</script>

<template>
<table>
  <tr>
    <th>Name</th>
    <th>Surname</th>
    <th>Age</th>
    <th>Salary</th>
    <th>Department</th>
  </tr>
  <tr v-for="item in listUsers">
    <td>{{item.name}}</td>
    <td>{{ item.surname }}</td>
    <td>{{item.age}}</td>
    <td>{{ item.salary }}</td>
    <td>{{item.department}}</td>
</tr>
  
</table>
</template>

<style scoped>

</style>
