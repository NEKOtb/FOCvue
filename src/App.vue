<script setup>
import { Suspense } from 'vue'
import CharacterCharacteristics from './components/CharacterCharacteristics.vue'
import CharactersMain from './components/CharactersMain.vue'
import AddCharacterMain from './components/AddCharacterMain.vue'
</script>

<template>
  <Suspense>
    <CharacterCharacteristics />
  </Suspense>
  <CharactersMain />
  <AddCharacterMain />
</template>

<style scoped></style>
