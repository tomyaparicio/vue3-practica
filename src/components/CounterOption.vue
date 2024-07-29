<template>
  <h3>{{ counter }}</h3>
  <button @click="addCounter">Incrementar</button>
  <button @click="lessCounter" class="decrementar">decrementar</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "CounterOption",
  components: {},

  data() {
    let counter = 0;
    return { counter };
  },

  methods: {
    addCounter() {
      this.counter++;
    },

    lessCounter() {
      this.counter--;
    },
  },
});
</script>

<style>
.decrementar {
  margin-left: 10px;
}
</style>
