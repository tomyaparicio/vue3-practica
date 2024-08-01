<template>
  <div>
    <input type="text" v-model="messege"/>
    <H3>{{ messege }}</H3>
    <h3>{{ reverseMessage }}</h3>
  </div>
</template>

<script lang="ts" setup>

import { ref, computed, Ref } from 'vue'

      let messege:Ref<string> = ref('')
      const reverseMessage:Ref<string> = computed(() => messege.value.split('').reverse().join(''))
  

 

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

<style scoped></style>