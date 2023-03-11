<template>
  <teleport to="body">
    <div class="modal">
      <h1>
        <slot name="title"/>
      </h1>
      <slot/>
      <button class="btn">hide modal</button>
    </div>
  </teleport>
</template>

<script setup>
import {useSlots} from "vue";

const slots = useSlots()

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