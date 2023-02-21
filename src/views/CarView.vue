<script setup>
  import {useRoute} from "vue-router"
  import cars from "../data/cars.json"

  const route = useRoute();

  const car = cars.find(c => c.id === parseInt(route.params.id));
</script>
<template>
  <div>
    <h1>Car View</h1>
    <p>Name: {{car.name}}</p>
    <p>Year: {{car.year}}</p>
    <p>Price: {{car.price}}</p>
    <RouterView/>
  </div>
</template>