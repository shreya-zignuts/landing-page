<script setup>
import NavbarComponent from "./components/NavbarComponent.vue";
import HomeComponent from "./components/HomeComponent.vue";
import ServiceComponent from "./components/ServiceComponent.vue";
import "../src/assets/css/style.css";
</script>

<template>
  <header>
    <NavbarComponent />
  </header>
  <main>
    <HomeComponent />
    <ServiceComponent />
  </main>
</template>

<style scoped></style>
