<template>
  <div class="home">
    <h2 ref="appTitleRef">{{ appTitle }}</h2>
    <h3>{{ counterData.title }}</h3>
    <div class="wrapper">
      <button @click="decreaseCounter(1)" class="btn">-</button>
      <span class="counter">{{ counterData.count }}</span>
      <button @click="increaseCounter(1)" class="btn">+</button>
    </div>
    <div>This counter is {{ oddOrEven }}</div>
    <div class="edit">
      <h3> Edit counters Title</h3>
      <input type="text" v-model="counterData.title" v-autofocus>
    </div>
  </div>
</template>

<script setup>

import {reactive, computed, watch, onMounted, ref, nextTick} from "vue";
import {vAutofocus} from "@/directives/vAutofocus";
/*const counter = ref(0)
const counterTitle = ref('tle')*/

const oddOrEven = computed(() => {
  if (counterData.count % 2 === 0) return 'even'
  return 'odd'
})
const appTitle = 'My counter App'

const appTitleRef = ref(null)
const counterData = reactive({
  count: 10,
  title: 'Counter title'
})
onMounted(() => {
  appTitleRef.value
})
watch(() => counterData.count, (newCount) => {
  if (newCount === 20) alert('someMSG')
})

const increaseCounter = async (val) => {
  counterData.count += val
  await nextTick(()=> {
    console.log('do smth')
  })
}

const decreaseCounter = (val) => {
  counterData.count -= val
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

