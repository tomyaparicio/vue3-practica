<template>
  <ul>
    <li v-for="country in countries" :key="country.id">
      {{ country.name }}
    </li>
  </ul>
</template>

<script lang="ts" setup>
import { ref } from "vue";

let countries = ref([
  {
    id: 1,
    name: "Argentina",
  },
  {
    id: 2,
    name: "Francia",
  },
  {
    id: 3,
    name: "España",
  },
  {
    id: 4,
    name: "UK",
  },
  {
    id: 5,
    name: "Italia",
  },
]);
</script>

<style></style>
