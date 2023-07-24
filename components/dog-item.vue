<script lang="ts" setup>
import { Dog } from "../entities";

defineProps<{
  dog: Dog;
}>();
</script>

<template>
  <div>
    <h3>{{ dog.name }}</h3>
    <p>{{ dog.bredd }}</p>
    <p>{{ dog.birthdate }}</p>
  </div>
</template>

<style scoped></style>
