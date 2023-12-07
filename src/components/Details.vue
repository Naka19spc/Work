<script setup></script>

<template>

  <div class="info-container">
    <div class="main-container">
      <h1>Detail Information</h1>
      <div class="input-container">
        <input class="inpt" value="Name" />
        <input class="inpt" value="Surname" />
        <input class="inpt" value="Age" />
        <input class="inpt" value="Salary" />

        <select class="inpt" name="Department" id="Department">
          <option value="volvo">It Department</option>
          <option value="saab">Finance Department</option>
          <option value="opel">Department of Tourism</option>
          <option value="audi">Medical Department</option>
        </select>
      </div>
    </div>
    <div>
      <h2>Table</h2>
    </div>
  </div>
</template>

<style>

.input-container {
  width: 200px;
  height: 100vw;
  background-color: hsla(160, 100%, 37%, 1);
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
</style>
