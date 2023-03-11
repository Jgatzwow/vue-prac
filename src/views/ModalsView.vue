<template>
  <div>
    <button class="btn" @click="toggleModal">show modal</button>
    <modal v-if="showModal" title="My modal title (via prop)" @hideModal="toggleModal">
      <p>Some text children like in react</p>
    </modal>
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