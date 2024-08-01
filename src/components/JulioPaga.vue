<template>
<v-row class="mx-2 my-2">
<v-col cols="6">
   <v-text-field 
   dense
   type="number" 
   v-model="subtotal"
   outlined
   > </v-text-field>
   <h3>Total Impuesto a Pagar ${{ totalVat }} ({{ vat }}%)</h3>           
   <v-spacer></v-spacer>
  <v-btn color="primary" >hola</v-btn>
</v-col>
</v-row>
</template>

<script lang="ts" setup>
  import { ref, computed } from 'vue'
const vat = 21
let subtotal = ref(0)

const totalVat = computed(() => vat*subtotal.value/100)

</script>

<style scoped></style>