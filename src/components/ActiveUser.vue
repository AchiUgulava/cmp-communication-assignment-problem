<script setup>
import {defineProps} from 'vue';
defineProps({
  username: {
    type: String,
    required: true,
  }, age: {
    type: Number,
    required: true,
  }
});
</script>
<template>
  <div class="container">
    <h1>User Name: {{username}}</h1>
    <h3>Age:<br>{{age}}</h3>
  </div>
</template>
<style>
div{
  text-align: center;
}

</style>