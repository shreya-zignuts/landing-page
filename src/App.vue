<script setup>
import NavbarComponent from "./components/NavbarComponent.vue";
import HomeComponent from "./components/HomeComponent.vue";
import ServiceComponent from "./components/ServiceComponent.vue";
import HealthcareComponent from "./components/HealthcareComponent.vue";
import DownloadComponent from "./components/DownloadComponent.vue";
import "../src/assets/css/style.css";
</script>

<template>
  <header>
    <NavbarComponent />
  </header>
  <main>
    <HomeComponent />
    <ServiceComponent />
    <HealthcareComponent />
    <DownloadComponent />
  </main>
</template>

<style scoped></style>
