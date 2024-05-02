<script setup></script>
<template>
  <div class="container">
    <p class="title">TITLE_NAME</p>
    <div class="add"><p>+</p></div>
  </div>
</template>
<style scoped>
.container {
  font-family: Inter, sans-serif;
  background-color: #283750;
  border-radius: 0.5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 400px;
  padding: 10px;
  .title {
    font-size: 1.5rem;
    color: #fff;
    margin-bottom: 10px;
  }
  .add {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #33435c;
    color: #1e293b;
    border-radius: 0.5rem;
    height: 40px;
    width: 100%;
    p {
      font-size: 1.5rem;
      font-weight: 700;
    }
  }
}
</style>
