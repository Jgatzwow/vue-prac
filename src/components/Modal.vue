<template>
  <teleport to="body">
    <div class="modal">
      <h1>this is a modal</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil, sunt?</p>
      <button class="btn">hide modal</button>
    </div>
  </teleport>
</template>

<script>

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