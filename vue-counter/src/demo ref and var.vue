<script setup>
import { ref } from 'vue'

// 非響應式
let normalCount = 0

// 響應式
const reactiveCount = ref(0)

function increase1() {

  normalCount++        // 不會更新畫面
}

function increase2() {
  reactiveCount.value+=5 // 畫面會更新
normalCount++        // 不會更新畫面
}
</script>

<template>
  <div>
    <p>普通變數：{{ normalCount }}</p>
    <p>ref 變數：{{ reactiveCount }}</p>
    <button @click="increase1">增加normal</button>
    <button @click="increase2">增加ref</button>
  </div>
</template>
