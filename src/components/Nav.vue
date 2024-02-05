<template>
  <div>
    <RouterLink active-class="active" to="/">Home</RouterLink>
    <RouterLink active-class="active" to="/about">About</RouterLink>
  </div>
</template>

<style scoped>
.active {
  font-weight: bold;
  color: rgb(241, 162, 14);
}
</style>
