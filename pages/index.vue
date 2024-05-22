<template>
  <div class="container">
    <div class="image-container">
      <h3>Hello world</h3>
      <img alt="new-nuxt-logo" src="~/assets/images/logo-uwu.png" />
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.container {
  margin-top: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.image-container img {
  margin: 0 auto;
  display: block;
  width: 80%;
  height: 80%;
}

h3 {
  font-size: 36px;
  color: rgb(14, 168, 106);
  text-align: center;
  padding: 0;
  margin: 0;
}
</style>