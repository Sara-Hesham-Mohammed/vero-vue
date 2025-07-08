<script setup>
import { ref } from 'vue'

const items = ref([
  {
    heading: 'Item 1',
    desc: "This is item one's desc",
    img: 'https://images.unsplash.com/photo-1512499617640-c2f999018b72?auto=format&fit=crop&w=800&q=80',
  },
  {
    heading: 'Item 2',
    desc: "This is item two's desc",
    img: 'https://images.unsplash.com/photo-1580894732444-f288cc8a943e?auto=format&fit=crop&w=800&q=80',
  },
  {
    heading: 'Item 3',
    desc: "This is item three's desc",
    img: 'https://images.unsplash.com/photo-1508253578933-e03c09f06b1c?auto=format&fit=crop&w=800&q=80',
  },
])
</script>

<template>
  <div v-for="item in items" :key="item" class="component">
    <img :src="item.img" alt="Image" />
    <h1>{{ item.heading }}</h1>
    <p>{{ item.desc }}</p>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
  .component {
    background-color: azure;
  }
}
</style>
