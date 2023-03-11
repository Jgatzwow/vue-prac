<template>
  <teleport to="body">
    <div class="modal">
      <h1>
        {{ title }}
      </h1>
      <slot/>
      <button @click="handleButtonClick" class="btn">hide modal</button>
    </div>
  </teleport>
</template>

<script setup>
import {useSlots} from "vue";

const slots = useSlots()

const props = defineProps({
  title: {
    type: String,
    default: '123'
  }
})
const emit = defineEmits(['hideModal'])

const handleButtonClick = () => {
  emit('hideModal')
}
</script>

<style scoped>
.modal {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  left: 0;
  top: 0;
  height: 100%;
  width: 100%;
  background: beige;
  padding: 10px;
}
</style>