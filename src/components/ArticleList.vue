<template>
  <section class="article-section" id="articles">
    <h2 class="article-heading">Check out our latest article</h2>
    <div class="title-line"></div>
    <div class="article-grid">
      <div v-for="(article, index) in articles" :key="index" class="article-card">
        <img :src="article.image" alt="Article Image" class="article-image" />
        <div class="article-content">
          <h3 class="article-title">{{ article.title }}</h3>
          <p class="article-description">{{ article.description }}</p>
          <a href="#" class="read-more">Read more ➔</a>
        </div>
      </div>
    </div>
    <div class="button-container">
      <button class="view-all-btn">View All</button>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

// Use dynamic import for images
const articles = ref([
  {
    image: new URL("@/assets/images/home/Mask Group.png", import.meta.url).href,
    title: "Disease detection, check up in the laboratory",
    description:
      "In this case, the role of the health laboratory is very important to do a disease detection...",
  },
  {
    image: new URL("@/assets/images/home/Mask Group (1).png", import.meta.url).href,
    title: "Herbal medicines that are safe for consumption",
    description:
      "Herbal medicine is very widely used at this time because of its very good for your health...",
  },
  {
    image: new URL("@/assets/images/home/Mask Group (2).png", import.meta.url).href,
    title: "Natural care for healthy facial skin",
    description:
      "A healthy lifestyle should start from now and also for your skin health. There are some...",
  },
]);
</script>

<style scoped></style>
