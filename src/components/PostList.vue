<template>
  <div class="container2">
    <PostDetail
      v-for="elm in info"
      :key="elm.title"
      :title="elm.title"
      :content="elm.content"
      @sayHi="showAlert" 
      @hola="hola2"
      
    >
    </PostDetail>
  </div>
</template>

<script lang="ts" setup>
import PostDetail from "./PostDetail.vue";

interface Post {
  title: string;
  content: string;
}

let info: Array<Post> = [
  { title: "Post 1", content: "texto ejemplo 1" },
  { title: "Post 2", content: "texto ejemplo 2" },
  { title: "Post 3", content: "texto ejemplo 3" },
  { title: "Post 4", content: "texto ejemplo 4" },
  { title: "Post 5", content: "texto ejemplo 5" },
];


function showAlert(msg:string){
  alert(msg)
}

function hola2(hola4:string){
  alert(hola4)
}
</script>

<style scoped>
.container2 {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-around;
}
</style>
