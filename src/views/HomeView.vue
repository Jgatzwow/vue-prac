<template>
  <div class="home">
    <div class="wrapper">
      <button @click="decreaseCounter" class="btn">-</button>
      <span class="counter">{{ counter }}</span>
      <button @click="increaseCounter" class="btn">+</button>
    </div>
  </div>
</template>

<script setup>

import {ref} from "vue";

const counter = ref(0)

const increaseCounter = () => {
  counter.value++
}

const decreaseCounter = () => {
  counter.value--
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

