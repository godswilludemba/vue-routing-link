<script setup>
import cars from "../data/cars.json";
import { RouterLink } from "vue-router";
</script>

<template>
  <h1>Home View</h1>
  <div class="cars">
    <RouterLink
      :to="`/cars/${car.id}`"
      v-for="car in cars"
      :key="car.id"
      href=""
      >{{ car.name }}</RouterLink
    >
  </div>
</template>

<style scoped>
.cars {
  display: flex;
}

.cars a {
  text-decoration: none;
  width: 100%;
  color: black;
  box-shadow: 1px 1px 10px rgb(63, 41, 41, 0.2);
  margin: 10px;
  text-align: center;
}
</style>
