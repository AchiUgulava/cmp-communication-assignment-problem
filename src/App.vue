
<script setup>
import { ref } from 'vue'
import ActiveUser from "./components/ActiveUser.vue"
import UserData from "./components/UserData.vue"
const username = ref('hi');
const age = ref(15);
const addUserData = (un, a) => {
    username.value = un;
    age.value = parseInt(a);
}
</script>

<template>
    <div class="content">
        <ActiveUser class="box" :username="username" :age="age" />
        <UserData class="box" @add-user-data="addUserData" />
    </div>
</template>
<style>
.content {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.box {
    padding: 100px;
    margin: 50px;
    border-radius: 20px;
    background-color: rgb(28, 74, 75);
    border-width: 2px;
    border-style: outset;
}
</style>
