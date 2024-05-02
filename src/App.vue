<script setup>
import { Suspense } from 'vue'
import CharacterCharacteristics from './components/CharacterCharacteristics.vue'
import CharactersMain from './components/CharactersMain.vue'
import AddCharacterMain from './components/AddCharacterMain.vue'
import ListMenu from './components/ListMenu.vue'
import ItemTemplate from './components/ItemTemplate.vue'
</script>

<template>
  <Suspense>
    <CharacterCharacteristics />
  </Suspense>
  <CharactersMain />
  <AddCharacterMain />
  <ListMenu />
  <ItemTemplate />
</template>

<style scoped></style>
