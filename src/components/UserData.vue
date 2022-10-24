<script setup>
import {ref} from 'vue'
const age = ref(null);
const username = ref('');
</script>

<template>
  <div>
  <input type="text" v-model="username">
    <br>
    <input type="text" v-model="age">
    <button @click="$emit('addUserData',username,age)">Submit Data</button>
  </div>
</template>
<style>
div{
  display: flex;
  flex-direction: column;
  justify-content:center;
}
input{
  background-color:rgb(159, 210, 213);
  padding: 5px;
  border-radius: 20px;
}
button{
  margin-top: 20px;
  background-color:rgb(14, 54, 56);
  padding: 5px;
  border-radius: 20px;
}
</style>