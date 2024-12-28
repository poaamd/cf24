<script setup>
import { ref } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
const name = ref("");
</script>

<template>
  <input v-model="name" type="text" />
  <div class="hi">HI {{ name }}</div>
  <HelloWorld />
</template>

<style>
.hi {
  border: solid 1px red;
}
</style>
