<script setup>

const props = defineProps(['listUsers','deleteWorker'])
console.log("listuser123", props.listUsers);
function remove(item){
 props.deleteWorker(item)
}

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
  <tr v-for="(item,index) in listUsers " :key="index">
    <td>{{item.name}}</td> 
    <td>{{item.surname}}</td>
    <td>{{item.age}}</td>
    <td>{{item.salary}}</td>
    <td>{{item.department}}</td>
    <button @click="remove(item)">Remove</button>
</tr>
  
</table>
</template>

<style scoped>

</style>
