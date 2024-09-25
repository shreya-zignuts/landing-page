<template>
  <nav ref="navbar">
    <div class="logo-container">
        <img src="@/assets/images/logo/logo.png" alt="logo" class="logo" />
    </div>
    <ul class="navbar">
      <li><a href="#home">Home</a></li>
      <li><a href="#findadoctor">Find a Doctor</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#apps">Apps</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
      <li><a href="#articles">Articles</a></li>
      <li><a href="#aboutus">About Us</a></li>
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

<style scoped>
.navbar a.active {
  color: black;
  font-weight: bold;
  border-bottom: 2px solid black; /* Optional: add a bottom border to active link */
}
</style>
