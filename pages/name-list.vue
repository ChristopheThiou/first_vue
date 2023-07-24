<script lang="ts" setup>
const name = ref(["Jean", "Pierre", "Paul", "Jean-Paul"]);
const newName = ref("");

function addName() {
  name.value.push(newName.value);
}
</script>

<template>
  <ul>
    <li v-for="item of name">{{ item }}</li>
  </ul>
  <input type="text" v-model="newName" placeholder="Type a name ..." />
  <button @click="addName()">Click !</button>
</template>

<style scoped></style>
