<template>
  <div class="post">
    <h3>{{props.title }}</h3>
    <p>{{ props.content }}</p>
    <input type="text" v-model="messege">
    <button @click="handleClick">di Hola</button>
  </div>
</template>
<script lang="ts" setup>
import {defineProps, defineEmits, Ref, ref} from 'vue'

const props = defineProps({
  title: String,
  content: String,
})

const emit = defineEmits(['sayHi'])

const handleClick = () =>{
  emit("sayHi", messege.value)
}
let messege: Ref<string> = ref("")


// name: 'PostDetail',
// props:{
//     title:String,
//     content:String,
// },
// emits:["sayHi"],

</script>

<style scoped>
.post {
  width: 300px;
  height: auto;
  border-radius: 10px;
  background-color: antiquewhite;
  margin-top: 10px;
  margin-bottom: 10px;
  padding: 10px;
}
</style>
