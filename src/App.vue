<template>
  <v-app>
    <v-main>
      <Drawer/>
      <router-view />
      <Footer/>
    </v-main>
  </v-app>
</template>

<script setup>
  import Drawer from "./components/Drawer.vue"
  import Footer from "./components/Footer.vue"
</script>
<style scoped>

</style>
