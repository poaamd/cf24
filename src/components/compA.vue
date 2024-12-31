<script setup>
import { ref, onBeforeMount, onMounted } from "vue";
import compC from "./compC.vue";
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
  console.log("Comp A: Before Mount");
});

onMounted(() => {
  console.log("Comp A: on Mounted");
});
</script>

<template>
  <div class="border-red">
    inside Commponent A
    <div>
      counter : {{ counter }}
      <button @click="increase">increase</button>
      <button @click="decrease">decrease</button>
    </div>
    <compC />
  </div>
</template>

<style>
button {
  margin: 5px;
}
.border-red {
  border: solid 1px red;
  padding: 15px;
}
</style>
