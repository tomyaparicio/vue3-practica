<template>
  <form class="form">
    <input class="id" v-model="inputText" type="text" />
    <input v-model="agree" type="checkbox" /> Acepto Los terminos y condiciones
  </form>
  <select v-model="countries">
    <option v-for="country in countries" v-bind:key="country.id">
      {{ country.name }}
    </option>
  </select>

  <h3>{{ inputText }}</h3>
</template>

<script lang="ts" setup>
import { Ref, ref } from "vue";

interface Country {
  id: number;
  name: string;
}

let inputText: Ref<string> = ref("");
let agree: Ref<boolean> = ref(false);
let countries: Country[] = [
  {
    id: 1,
    name: "Argentina",
  },
  {
    id: 2,
    name: "Brasil",
  },
  {
    id: 3,
    name: "Italia",
  },
];
</script>

<style>
.id {
  border: 1px solid red;
  border-radius: 5px;
  margin-right: 10px;
}

.form {
  padding-top: 5px;
  padding-left: 5px;
}
</style>
