<script setup></script>

<template>
  <div class="container">
    <div class="add">
      <p>+</p>
    </div>
  </div>
</template>

<style scoped>
.container {
  cursor: pointer;
  font-family: Inter, sans-serif;
  position: relative;
  color: #192334;
  background-color: #192334;
  border-radius: 0.5rem;
  max-width: 280px;
  height: 340px;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  .add {
    background-color: #1e293b;
    height: 100px;
    width: 100px;
    border-radius: 99px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 5rem;
  }
}
</style>
