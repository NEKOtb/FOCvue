<script setup></script>

<template>
  <div class="container">
    <div class="image"></div>
    <div class="text">
      <p class="name">Лейнэ Армист</p>
      <p class="raceAndClass">Человек - Мистический рыцарь</p>
    </div>
  </div>
</template>

<style scoped>
.container {
  cursor: pointer;
  font-family: Inter, sans-serif;
  position: relative;
  color: #fff;
  background-color: #283750;
  border-radius: 0.5rem;
  max-width: 280px;
  padding: 10px;
  .image {
    background-color: #b1b1b1;
    height: 300px;
    border-radius: 0.5rem;
  }
  .text {
    margin-top: 5px;
    .name {
      font-size: 1.25rem;
      text-align: center;
    }
    .raceAndClass {
      font-size: 0.9rem;
      text-align: center;
    }
  }
}
</style>
