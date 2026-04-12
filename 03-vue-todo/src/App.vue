<script setup>
import {ref} from 'vue'
const newTask=ref('')
const todos=ref([])

const addTask = () =>{
    const text = newTask.value.trim()
    if (!text){
        return
    }

    todos.value.push({
        id: Date.now(),
        text: text,
        completed: false,
        favorite: false,
    })

    console.log(todos)
}

</script>

<template>
<div class="wrapper">
    <h1> Todo App</h1>
    <div class="input-row">
        <input type='text' v-model='newTask' placeholder='new todo enter here' />
        <button @click="addTask">Add</button>
    </div>
    <h2 >{{ newTask }}</h2>
</div>
</template>

<style scoped>
.app{
    max-width: 500;
    text-align: center;
    font-family: sans-serif;
    margin: 2rem auto;
}
h2{
    color:darkorange;
    background-color: lightblue;
    width: fit-content;
    padding: 0 2rem;
}
</style>
