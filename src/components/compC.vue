<script setup>
import { ref, onBeforeMount, onMounted } from "vue";
const counter = ref(0);
const increase = () => {
  console.log(":inside of increment func");

  counter.value = counter.value + 1;
};

const decrease = () => {
  console.log(":inside of decrease func");

  counter.value = counter.value - 1;
};

onBeforeMount(() => {
  console.log("Comp C: Before Mount");
});

onMounted(() => {
  console.log("Comp C: on Mounted");
});
</script>

<template>
  <div class="border-white">
    inside Commponent C
    <div>
      counter : {{ counter }}
      <button @click="increase">increase</button>
      <button @click="decrease">decrease</button>
    </div>
  </div>
</template>

<style>
.border-white {
  border: solid 1px rgb(255, 255, 255);
  padding: 15px;
  margin: 15px;
}
</style>
