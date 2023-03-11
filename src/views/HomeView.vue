<template>
  <div class="home">
    <h2>{{appTitle}}</h2>
    <h3>{{ counterData.title }}</h3>
    <div class="wrapper">
      <button @click="decreaseCounter" class="btn">-</button>
      <span class="counter">{{ counterData.count }}</span>
      <button @click="increaseCounter" class="btn">+</button>
    </div>
    <div class="edit">
      <h3> Edit counters Title</h3>
      <input type="text" v-model="counterData.title ">
    </div>
  </div>
</template>

<script setup>

import {reactive} from "vue";

/*const counter = ref(0)
const counterTitle = ref('tle')*/

const appTitle = 'My counter App'

const counterData = reactive({
  count: 10,
  title: 'Counter title'
})

const increaseCounter = () => {
  counterData.count++
}

const decreaseCounter = () => {
  counterData.count--
}

</script>


<style>
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}

.btn {
  padding: 10px 20px;
  background: none;
  border: 1px solid #42b983;
}

.btn:hover {
  background: #42b983;
}
</style>

