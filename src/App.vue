<template>
  <CarsCards :cars="euCars" />
  <cars-cards :cars="asCars" />
  <!-- slot used here -->
  <card>
    <p>EU Cars</p>
    <p>Total: {{ euCars.length }}</p>
  </card>
  <card>
    <p>Asian Cars</p>
    <p>Total: {{ asCars.length }}</p>
  </card>
</template>

<script>
import { ref } from 'vue'
import CarsCards from '@/components/CarsCard.vue'
import asCarsData from '@/data/asian-cars.js'
import euCarsData from '@/data/eu-cars.js'
import Card from '@/components/CardTemp.vue'

export default {
  name: 'App',
  components: {
    CarsCards,
    Card
  },
  setup () {
    const euCars = ref(euCarsData)
    const asCars = ref(asCarsData)

    return { euCars, asCars }
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
