<template>
  <nav>
    <div class="logo-container">
      <div class="logo-wrapper">
        <img src="@/assets/images/logo/ellipse.png" alt="ellipse" class="logo-ellipse" />
        <img src="@/assets/images/logo/T.png" alt="T" class="logo-t" />
      </div>
      <h2 class="logo-text">Trafalgur</h2>
    </div>
    <ul class="navbar">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">Find a doctor</a></li>
      <li><a href="#languages">Apps</a></li>
      <li><a href="#portfolio">Testimonials</a></li>
      <li><a href="#achievement">About us</a></li>
    </ul>
    <div id="menu-icon" class="bx bx-menu"></div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const navbar = ref(null);

const handleScroll = () => {
  if (navbar.value) {
    if (window.scrollY > 50) {
      // Adjust the scroll value as needed
      navbar.value.classList.add("scrolled");
    } else {
      navbar.value.classList.remove("scrolled");
    }
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped></style>
