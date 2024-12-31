<script setup>
import CompC from  "@/components/CompC.vue";
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated } from "vue";

onBeforeMount(() => {
  console.log("Comp A: Before Mount");
});
onMounted(() => {
  console.log("Comp A: on Mounted");
});

const counter = ref(0);
const increment = () => {
  console.log("Inside Increment Func");
  counter.value = counter.value + 1;
};

onBeforeUpdate(() => {
  console.log("Comp A: Before Update");
});
onUpdated(() => {
  console.log("Comp A: on Updated");
});

console.log("Comp A: On Created");
</script>

<template>
  <div class="border-red">
    <div>Inside Component A</div>
    <div>
      Counter: {{ counter }}
      <button @click="increment">Add</button>
    </div>
    <CompC />
    <div v-if="counter===5" >hoora</div>
    <div v-else-if="counter===6">hello</div>
    <div v-else> vaay</div>
  </div>
</template>

<style scoped>
.border-red {
  border: solid 1px red;
  padding: 12px;
}
</style>