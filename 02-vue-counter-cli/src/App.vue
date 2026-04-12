<script setup>
import { ref} from 'vue'
const counter = ref(0)
const counterMinus = () => {
  counter.value-=4
}
</script>

<template>
  <h1>Counter is: {{counter}}</h1>
  <button @click="counter+=8">Counter+</button>
  <button @click="counterMinus">Counter-</button>
  <hr/>
  <h1>Hello World!</h1>
</template>

<style scoped></style>
