<script setup>
let ItemTitle = 'ItemNameLongLongLongName'
let ItemType = 'Ammunition'
let modifyStatus = '+0'
let damageType = 'Рубящий1К8'
let armorStatus = '15'
let armorModify = '10 + ЛОВК'
let importantMark = false
let countStatus = 5
</script>
<template>
  <div class="container">
    <p class="title">{{ ItemTitle }}</p>
    <div class="stats">
      <div v-if="ItemType == 'Weapon'" class="modifyStatus boxView">{{ modifyStatus }}</div>
      <div v-if="ItemType == 'Weapon'" class="damageType boxView">{{ damageType }}</div>
      <div v-if="ItemType == 'Armor'" class="armorStatus boxView">{{ armorStatus }}</div>
      <div v-if="ItemType == 'Armor'" class="armorModify boxView">{{ armorModify }}</div>
      <div v-if="ItemType == 'Ammunition'" class="countMinus boxView">-</div>
      <div v-if="importantMark == true" class="importantMark boxView">ВАЖНОЕ</div>
      <div v-if="ItemType == 'Ammunition'" class="countStatus boxView">{{ countStatus }} шт.</div>
      <div v-if="ItemType == 'Ammunition'" class="countPlus boxView">+</div>
      <div class="editBtn boxView">Edit</div>
    </div>
  </div>
</template>
<style scoped>
.container {
  font-family: Inter, sans-serif;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  flex-wrap: nowrap;
  gap: 5px;
  padding: 5px;
  color: #fff;
  background-color: #1e293b;
  height: 40px;
  width: 100%;
  border-radius: 0.5rem;
  .stats {
    display: flex;
    gap: 5px;
  }
  .importantMark {
    background-color: #fdcb4b;
    color: #000;
  }
}
.boxView {
  background-color: #33435c;
  height: 100%;
  border-radius: 3px;
  padding: 3px;
  text-wrap: nowrap;
  text-align: center;
  min-width: 30px;
}
</style>
