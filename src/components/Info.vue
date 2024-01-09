<script setup>
const props = defineProps(['name','surname','age','salary','department'])
console.log("teest",props.name);
</script>
<template>
<ul>
    <li>I am: {{props.name }}</li>
    <li>My Surname is: {{ props.surname }}</li>
    <li>My age is: {{ props.age }}</li>
    <li>My salary is: {{ props.salary }}</li>
    <li>My department is: {{props.department }}</li>
</ul>

</template>