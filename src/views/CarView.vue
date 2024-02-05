<script setup>
import { useRoute, useRouter, RouterView } from "vue-router";
import cars from "../data/cars.json";

const route = useRoute();
const router = useRouter();

const carId = parseInt(route.params.id);
const car = cars.find((c) => c.id === carId);

const showContact = () => {
  if (carId === 4) return;
  return router.push(`/cars/${carId}/contact`);
};
</script>

<template>
  <div>
    <h1>Cars View</h1>
    <p>{{ car.name }}</p>
    <p>{{ car.description }}</p>
    <p>{{ car.price }}</p>
    <p>{{ car.year }}</p>

    <button @click="showContact">Contact Info</button>

    <RouterView />
  </div>
</template>
