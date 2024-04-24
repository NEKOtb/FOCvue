<script setup>
import { ref } from 'vue'

let Index = 0
let DefSetups
const fResult = await fetch('/default_data/DefaultCharacterSetups.json')
  .then((res) => res.json())
  .then((data) => {
    DefSetups = data.CharacteristicsDatas
  })
// console.log(DefSetups)

let CharacteristicsName = DefSetups[Index].name
let CharacteristicsLevel = DefSetups[Index].level

let ModifyLevel = (CharacteristicsLevel) => {
  switch (CharacteristicsLevel) {
    case 1:
      return -5
      break
    case 2:
      return -4
      break
    case 3:
      return -4
      break
    case 4:
      return -3
      break
    case 5:
      return -3
      break
    case 6:
      return -2
      break
    case 7:
      return -2
      break
    case 8:
      return -1
      break
    case 9:
      return -1
      break
    case 10:
      return '+0'
      break
    case 11:
      return '+0'
      break
    case 13:
      return '+1'
      break
    case 12:
      return '+1'
      break
    case 14:
      return '+2'
      break
    case 15:
      return '+2'
      break
    case 16:
      return '+3'
      break
    case 17:
      return '+3'
      break
    case 18:
      return '+4'
      break
    case 19:
      return '+4'
      break
    case 20:
      return '+5'
      break
    case 21:
      return '+5'
      break
    case 22:
      return '+6'
      break
    case 23:
      return '+6'
      break
    case 24:
      return '+7'
      break
    case 25:
      return '+7'
      break
    case 26:
      return '+8'
      break
    case 27:
      return '+8'
      break
    case 28:
      return '+9'
      break
    case 29:
      return '+9'
      break
    case 30:
      return '+10'
      break
  }
}

let SkillsNames = DefSetups[Index].skills
const checkActive = ref(false)

function checkActiveFunc() {
  console.log(checkActive)
  if (checkActive.value == false) {
    console.log('1')
    checkActive.value = true
  } else if (checkActive.value == true) {
    console.log('2')
    checkActive.value = false
  }
}
</script>

<template>
  <div class="container">
    <p class="name">{{ CharacteristicsName }}</p>
    <div class="numbers">
      <div>{{ CharacteristicsLevel }}</div>
      <div>{{ ModifyLevel(CharacteristicsLevel) }}</div>
    </div>
    <div class="skillArea">
      <div class="cont">
        <div class="check_s"></div>
        <div class="modify">{{ ModifyLevel(CharacteristicsLevel) }}</div>
        <p>СПАСБРОСОК</p>
      </div>
    </div>
    <!-- {{ checkActive }} -->
    <div class="skillArea" v-for="(item, Index) in SkillsNames">
      <div class="cont">
        <div
          class="check"
          :class="{ checked: checkActive }"
          @click="checkActiveFunc(checkActive)"
        ></div>
        <div class="modify">{{ ModifyLevel(CharacteristicsLevel) }}</div>
        <p>{{ SkillsNames[Index].name }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  font-family: Inter, sans-serif;
}
.container {
  max-width: 250px;
  background-color: #283750;
  border-radius: 0.7rem;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
  .name {
    font-size: 1.5rem;
    padding: 0px 10px;
  }
  .numbers {
    width: 100%;
    padding: 5px 10px;
    display: flex;
    flex-direction: row;
    gap: 0.5rem;
    font-size: 1.5rem;
    font-weight: bold;

    div {
      flex: 1 1;
      padding: 5px;
      padding-right: 15px;
      background-color: #1e293b;
      border-radius: 0.5rem;
      text-align: center;
      align-self: center;
    }
    :first-child {
      flex: 2 1;
      text-align: right;
      font-size: 1.7rem;
    }
  }
  .skillArea {
    width: 100%;
    padding: 5px 10px;
  }
  .cont {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 0.5rem;
    border-radius: 0.5rem;
    background-color: #1e293b;
    .check_s {
      cursor: pointer;
      margin-left: 10px;
      min-width: 15px;
      min-height: 15px;
      border: solid 3px #496698;
      transform: rotate(45deg);
    }
    .checked_s {
      cursor: pointer;
      margin-left: 10px;
      min-width: 15px;
      min-height: 15px;
      border: solid 3px #496698;
      transform: rotate(45deg);
      background-color: #496698;
    }
    .check {
      cursor: pointer;
      margin-left: 9px;
      width: 19px;
      height: 19px;
      border-radius: 98px;
      border: solid 3px #496698;
    }
    .checked {
      cursor: pointer;
      margin-left: 9px;
      width: 19px;
      height: 19px;
      border-radius: 98px;
      border: solid 3px #496698;
      background-color: #496698;
    }
    .modify {
      margin: 5px;
      padding: 2px 5px;
      border-radius: 3px;
      background-color: #283750;
    }
  }
}
</style>
