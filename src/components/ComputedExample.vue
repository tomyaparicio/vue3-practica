<template>
  <v-row class="mx-2 my-2">
    <v-col cols="6" class="box">
    <v-text-field type="text" v-model="messege"></v-text-field>
    <H3>{{ messege }}</H3>
    <h3>{{ reverseMessage }}</h3>
    <v-spacer></v-spacer>
    <v-btn class="boton" color="primary">hola</v-btn>
    </v-col>
  </v-row>
</template>

<script lang="ts" setup>

import { ref, computed, Ref } from 'vue'

      let messege= ref('')
      const reverseMessage = computed(() => messege.value.split('').reverse().join(''))
  

// OPTION API

// import { defineComponent } from 'vue';

// export default defineComponent ({
//     name: "ComputedExample",
//     data() {
//         return {
//             messege: ''
//         }
//     },
//     computed: {
//         reverseMessage(): string {
//             return this.messege.split('').reverse().join('')
//         }
//     }


//})  

</script>



<style scoped>
.box{ 
  padding: 10px;
  margin: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
.boton{
  margin-top: 10px;
  margin-bottom: 10px;

}
</style>