<script setup lang="ts">
import OneCar from '@/components/main-page/OneCar.vue'

const allCars = [
  {
    name: 'Koenigsegg',
    type: 'Sport',
    photo: '/cars/koenigsegg.png',
    fuel_tank: '90L',
    transmission: 'Manual',
    people: '2 People',
    price: 120
  },
  {
    name: 'Nissan GT - R',
    type: 'Sport',
    photo: '/cars/nissan.png',
    fuel_tank: '80L',
    transmission: 'Manual',
    people: '2 People',
    price: 80
  },
  {
    name: 'Rolls - Royce',
    type: 'Sedan',
    photo: '/cars/rolls-royce.png',
    fuel_tank: '70L',
    transmission: 'Manual',
    people: '4 People',
    price: 110
  }
]
</script>

<template>
  <OneCar
    v-for="car in allCars"
    :name="car.name"
    :type="car.type"
    :photo="car.photo"
    :fuel_tank="car.fuel_tank"
    :transmission="car.transmission"
    :people="car.people"
    :price="car.price"
  />
</template>
