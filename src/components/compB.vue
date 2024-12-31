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
  console.log("Comp B: Before Mount");
});

onMounted(() => {
  console.log("Comp B: on Mounted");
});
</script>

<template>
  <div class="border-blue">
    inside Commponent B
    <div>
      counter : {{ counter }}
      <button @click="increase">increase</button>
      <button @click="decrease">decrease</button>
    </div>
  </div>
</template>

<style>
.border-blue {
  border: solid 1px rgb(42, 0, 94);
  padding: 15px;
}
</style>
