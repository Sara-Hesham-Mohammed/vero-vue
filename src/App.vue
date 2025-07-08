<script setup>
import { ref } from 'vue'
import Component from './components/Component.vue'

const itemsArr = ref([10, 20, 30, 40])
let num = ref(0)

function doSomething() {
  console.log('CLICKING')
  num.value++
}
</script>

<template>
  <header></header>

  <main>
    <a @click="doSomething" class="linkk"> Click here </a>
    <p>Number {{ num }}</p>

    <ul>
      <li v-for="item in itemsArr" :key="item">Item {{ item }}</li>
    </ul>
  </main>

  <Component></Component>
</template>

<style scoped>
@media (min-width: 1024px) {
  .linkk:hover {
    text-decoration: underline;
  }
}
</style>
