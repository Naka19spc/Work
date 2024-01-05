<script setup>
import { ref } from 'vue';
import Tables from './Tables.vue'
import Info from './Info.vue';


const  name =ref('')
const surname =ref('');
const age =ref('');
const salary =ref('');
const department =ref('');
const workers =ref([{
  name:"avto",
  surname:'Zen',
  age:28,
  salary:123,
  department:'tourism'
}]);
function add(){
  console.log("teest",name.value, surname.value, age.value, salary.value, department.value);
  const newWorker ={
    name: name.value,
    surname: surname.value,
    age:age.value,
    salary:salary.value,
    department:department.value,
  
  }
  if(name.value == '' || surname.value ==''){
    alert("There is no name and surname")

  }else{

    console.log("newworker", newWorker);
   workers.value.push(newWorker)
   name.value =""
   surname.value =""
   age.value=""
   salary.value =""
   department.value=""
  }

}

</script>


<template>

  <div class="info-container">
    <div class="main-container">
      <h1>Detail Information</h1>
      <div class="input-container">
        <input class="inpt"  type="text" v-model="name" />
        <input class="inpt"  type="text" v-model="surname" />
        <input class="inpt"  type="Number" v-model="age"/>
        <input class="inpt"  type="Number" v-model="salary" />

        <select class="inpt" name="Department" id="Department" v-model="department" >
          <option value="it">It Department</option>
          <option value="finance">Finance Department</option>
          <option value="tourism">Department of Tourism</option>
          <option value="medical">Medical Department</option>
        </select>
        <button @click="add" class="subButt">Submit</button>
        
      </div>
      <Info/>
      <Tables :listUsers = "workers" />
    </div>

  </div>
</template>

<style>

.input-container {
  width: 200px;
  /* height: 100vw; */
  background-color: rgb(255, 255, 255);
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 40px;
}
.inpt {
  height: 25px;
  border: 1px black solid;
  border-radius: 10px;
}
.info-container {
  display: flex;

  justify-content: space-around;
}

.subButt{
 border: 1px solid black;
 border-radius: 10px;
 height: 25px;
background-color:  hsla(160, 100%, 37%, 1);
cursor: pointer;
}
.lists{
 list-style: none;
}
</style>
