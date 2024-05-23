<script setup>
const route = useRoute()
const isNewNuxtLogo = ref(null)
const isOldNuxtLogo = ref(null)
// alternatively store the info in a cookie
const uwuCookie = useCookie('uwu-mode', {
  default: () => false
})
isNewNuxtLogo.value = uwuCookie.value

watch(() => route.fullPath, () => {
  if (route.fullPath === '/?new') {
    isNewNuxtLogo.value = true
    isOldNuxtLogo.value = false
  } else if (route.fullPath === '/?old') {
    isOldNuxtLogo.value = true
    isNewNuxtLogo.value = false
  } else if (route.fullPath === '/') {
    isNewNuxtLogo.value = true
    isOldNuxtLogo.value = false
  }
}, { immediate: true })




</script>
<template>
  <div class="container">
    <div class="image-container">
      <h3>Hello world</h3>
      <img v-if="isNewNuxtLogo" alt="New nuxt logo" src="~/assets/images/logo-uwu.png" />
      <img v-if="isOldNuxtLogo" alt="Old nuxt logo" src="~/assets/images/old-nuxt-logo.png" />
    </div>
  </div>
</template>

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