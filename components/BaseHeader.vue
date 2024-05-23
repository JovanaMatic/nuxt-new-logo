<template>
  <div>
    <ul>
      <NuxtLink class="links active" to="/">Home</NuxtLink>
      <NuxtLink class="links" to="old-logo">Old logo</NuxtLink>
      <NuxtLink class="links" to="new-logo">New logo</NuxtLink>
    </ul>
  </div>
</template>

<script setup>

</script>

<style scoped>

  ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

.links {
  float: left;
}

.links {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

.links:hover:not(.active) {
  background-color: #111;
}

.active {
  background-color: #04AA6D;
}
</style>