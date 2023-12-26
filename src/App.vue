<script setup>

import Header from './components/Header.vue';
import Details from './components/Details.vue'
import Tables from './components/Tables.vue'


</script>

<template>

<Header/>
<div class="body">
<Details/>

</div>

</template>

<style scoped>
header {
  line-height: 1.5;
}

.body{
  display: flex;
  flex-direction: row;
  justify-content: space-around;

}


</style>
