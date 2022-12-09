<template>
  <div class="card">
    <div id="preview">
        <img :src="post.img">
    </div>
    <div id="info">
        <h2>{{post.title}}</h2>
        <h4>{{post.description}}</h4>
        <p>{{post.content}}</p>
    </div>
  </div>
</template>

<script setup>

const props = defineProps(["post"]);

</script>

<style>
.card{
    width: 33%;
}
</style>