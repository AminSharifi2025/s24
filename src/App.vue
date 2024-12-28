<script setup>
import { ref } from 'vue';
import HelloWorld from "./components/HelloWorld.vue";
// export default{
//   setup:()=>{
    const message ="Amin";
    const name =ref("");
//     return{
//       message,
//     };
//   },
// };
</script>

<template>
<HelloWorld/>
  <input v-model="name" type="text">

  <div class="hi">hi{{ name }}</div>
</template>



<style>
.hi{
  border: solid 1px red;
}
</style>