<script setup>
import NavbarComponent from "./components/NavbarComponent.vue";
import HomeComponent from "./components/HomeComponent.vue";
import ServiceComponent from "./components/ServiceComponent.vue";
import HealthcareComponent from "./components/HealthcareComponent.vue";
import DownloadComponent from "./components/DownloadComponent.vue";
import TestimonialComponent from "./components/TestimonialComponent.vue";
import ArticleList from "./components/ArticleList.vue";
import FooterComponent from "./components/FooterComponent.vue";
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
    <TestimonialComponent />
    <ArticleList />
    <footer>
      <FooterComponent />   
    </footer>
  </main>
</template>

<style scoped></style>
