<template>
  <section class="testimonial-section" id="testimonials">
    <div class="testimonial-container">
      <!-- Testimonial Card -->
      <div class="carousel-card">
        <h2 class="section-title">What our customers are saying</h2>
        <div class="divider"></div>
        <div class="testimonial-content">
          <!-- Left Side: Photo and Info -->
          <div class="testimonial-left">
            <div class="photo-container">
              <img
                :src="testimonials[activeIndex].image"
                alt="Profile Image"
                class="testimonial-image"
              />
            </div>
            <div class="testimonial-info">
              <h5>{{ testimonials[activeIndex].name }}</h5>
              <p>{{ testimonials[activeIndex].title }}</p>
            </div>
          </div>

          <!-- Right Side: Quote -->
          <div class="testimonial-right">
            <blockquote>
              <p>
                {{ testimonials[activeIndex].quote }}
              </p>
            </blockquote>
          </div>
        </div>
      </div>

      <!-- Carousel Controls -->
      <div class="carousel-controls">
        <button class="carousel-control-prev" @click="prevSlide" :class="{ active: activeIndex > 0 }">
          <span>
            <img src="@/assets/images/home/arrow-left-solid.svg" alt="Previous" />
          </span>
        </button>
        <div class="carousel-indicators">
          <span
            v-for="(item, index) in testimonials.length"
            :key="index"
            :class="{ active: index === activeIndex }"
            @click="goToSlide(index)"
          ></span>
        </div>
        <button
          class="carousel-control-next"
          @click="nextSlide"
          :class="{ active: activeIndex < testimonials.length - 1 }"
        >
          <span>
            <img src="@/assets/images/home/arrow-right-solid.svg" alt="Next" />
          </span>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const testimonials = ref([
  {
    image: "https://m.media-amazon.com/images/I/41B3Q0XgFVL.jpg",
    name: "Edward Newgate",
    title: "Founder Circle",
    quote:
      "“Our dedicated patient engagement app and web portal allow you to access information instantaneously (no tedious forms, long calls, or administrative hassle) and securely.”",
  },
  {
    image: "https://m.media-amazon.com/images/I/41ONa5HOwfL.jpg",
    name: "Alice Johnson",
    title: "CEO of TechWorld",
    quote:
      "“The platform has transformed the way we work, improving productivity and collaboration across our teams.”",
  },
  {
    image: "https://m.media-amazon.com/images/I/41Brp3Gs6sL._AC_UF1000,1000_QL80_.jpg",
    name: "Michael Smith",
    title: "Product Manager at InnovateX",
    quote:
      "“A game-changer in the industry, providing solutions that streamline complex processes effortlessly.”",
  },
]);

const activeIndex = ref(0);

const prevSlide = () => {
  activeIndex.value =
    activeIndex.value > 0 ? activeIndex.value - 1 : testimonials.value.length - 1;
};

const nextSlide = () => {
  activeIndex.value =
    activeIndex.value < testimonials.value.length - 1 ? activeIndex.value + 1 : 0;
};

const goToSlide = (index) => {
  activeIndex.value = index;
};
</script>

<style scoped>
button {
  background: none;
  border: none;
  padding: 0;
  cursor: pointer;
}

button img {
  width: 40px;
  height: auto;
  margin: 10px 0 0 0;
  fill: #458ff683;
  transition: fill 0.3s ease;
}

button.active img {
  fill: #458ff6;
}

button:disabled img {
  opacity: 0.5;
  cursor: not-allowed;
}

.carousel-indicators span {
  display: inline-block;
  cursor: pointer;
  margin: 0 5px;
}

.carousel-indicators span img {
  width: 20px;
  height: auto;
  fill: #458ff683;
  transition: fill 0.3s ease;
}

.carousel-indicators span.active img {
  fill: #458ff6;
}
</style>

