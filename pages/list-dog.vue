<script lang="ts" setup>
import { Dog } from "entities";

const { data, refresh } = useFetch<Dog[]>("http://localhost:8000/api/dog");

async function postDog(dog:Dog){
  await $fetch('http://localhost:8000/api/dog', {
    method: 'POST',
    body: dog
  })
  refresh();
}
</script>

<template>
  <FormDog  @submit="postDog($event)"/>
  <DogItem v-for="item of data" :dog="item" />
</template>

<style scoped></style>
