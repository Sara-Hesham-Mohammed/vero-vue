<script setup>
import {ref} from 'vue'

const itemsArr = ref([10,20,30,40]);
let seen = ref(false);

function doSomething(){
  console.log('CLICKING');
  console.log(`before: ${seen.value}`);
  seen.value = !seen.value;
  console.log(`after: ${seen.value}`);
  
}
</script>

<template>
  <header>
  </header>

  <main>
    <a @click="doSomething"> Click here </a>
    <p v-if="seen">Now you see me</p>

    <ul>
      <li v-for="item in itemsArr" :key="item"> Item {{ item }}</li>
    </ul>
  </main>
</template>

<style scoped>

@media (min-width: 1024px) {

}
</style>
