<template>
  <div class="post">
    <h3>{{props.title }}</h3>
    <p>{{ props.content }}</p>
    <input type="text" v-model="messege">
    <input type="text" v-model="mensaje">
    <button @click="handleClick" class="boton1">boton1</button>
    <button  @click="holahola"> boton2</button>
  </div>
</template>
<script lang="ts" setup>
import {defineProps, defineEmits, Ref, ref} from 'vue'


// Prop = Se utiliza para conectar el componente padre a hijo
const props = defineProps({
  title: String,
  content: String,
})

// Emit = Se utiliza para conectar el componente hijo con el padre
const emit = defineEmits(['sayHi','hola'])

const handleClick = () =>{
  console.log(messege)
  emit("sayHi", messege.value)
}

const holahola =() =>{
  emit ("hola", mensaje.value)
}
// ---------------------------

let messege: Ref<string> = ref("")

let mensaje: Ref<string> = ref("")

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
