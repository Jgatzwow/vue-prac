<template>
  <div>
    <h2>some modal</h2>
    <button class="btn" @click="toggleModal">show modal</button>
    <modal v-if="showModal"></modal>
  </div>
</template>

<script setup>

import {ref} from "vue";
import Modal from "@/components/Modal.vue";
const showModal = ref(false)

const toggleModal = () => {
  showModal.value = !showModal.value
}
</script>

<style scoped>

</style>