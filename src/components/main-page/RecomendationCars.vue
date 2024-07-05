<script setup lang="ts">
import OneCar from '@/components/main-page/OneCar.vue'
import type Car from '@/types/cars'
import { defineProps } from 'vue'

const props = defineProps({
  cars: Array<Car>
})

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
  },
  {
    name: 'All New Rush',
    type: 'SUV',
    photo: '/cars/suzuki.png',
    fuel_tank: '70L',
    transmission: 'Manual',
    people: '4 People',
    price: 72
  },
  {
    name: 'CR  - V',
    type: 'SUV',
    photo: '/cars/vw.png',
    fuel_tank: '80L',
    transmission: 'Manual',
    people: '6 People',
    price: 80
  }
]

console.log(allCars)
</script>

<template>
  <OneCar
    v-for="car in props.cars"
    :name="car.name"
    :type="car.type"
    :photo="car.photo"
    :fuel_tank="car.fuel_tank"
    :transmission="car.transmission"
    :people="car.people"
    :price="car.price"
  />
</template>
