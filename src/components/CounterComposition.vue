<template>
  <h3>{{ counter }}</h3>
  <button @click="addCounter">Incrementar</button>
  <button @click="lessCounter">Incrementar</button>
</template>

<script lang="ts" setup>
import { type Ref, ref } from "vue";

let counter: Ref = ref(0);

const addCounter = (): void => {
  counter.value++;
  console.log(counter.value);
};

function lessCounter() {
  counter.value--;
  console.log(counter.value);
}
</script>
