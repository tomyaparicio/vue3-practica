<template>
    <div class="post-card">
        <h3>
            Titulo
        </h3>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. A, inventore? Porro voluptates repellendus error facere sequi eligendi maiores dolorem quasi. Veritatis aperiam reprehenderit repellendus id quis hic, ratione impedit totam.</p>
        <Postbuttom/>        
    </div>
</template>

<script lang="ts" setup>
import Postbuttom from './PostButton.vue'

</script>

<style scoped>
.post-card{
    border-radius: 15px;
    padding: 10px;
    margin: 5px;
    border: 1px solid #ccc;
}
</style>