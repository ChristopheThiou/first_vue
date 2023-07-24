<script lang="ts" setup>
import { Dog } from "entities";

const dog = ref<Dog>({ name: "", bredd: "", birthdate: "" });

const emit = defineEmits(["submit"]);

function handleSubmite() {
  emit("submit", dog.value);
}
</script>

<template>
  <form @submit.prevent="handleSubmite()">
    <label for="name">Name : </label>
    <input type="text" v-model="dog.name" placeholder="Type a name ..." />
    <label for="breed">Breed : </label>
    <input type="text" v-model="dog.bredd" placeholder="Type a breed ..." />
    <label for="birthdate">Birthdate : </label>
    <input
      type="date"
      v-model="dog.birthdate"
      placeholder="Type a birthdate ..."
    />
    <button>Add</button>
  </form>
</template>

<style scoped></style>
