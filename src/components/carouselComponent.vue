<script setup>
import { Carousel, Slide, Navigation } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';

const slides = [
  { type: 'text', content: 'Slide 2' },
  { type: 'text', content: 'Slide 3' },
];
</script>

<template>
  <div class="carousel-container">
    <Carousel class="h-[500px] w-full" :items-to-show="1" :wrap-around="true">
      <Slide v-for="(slide, index) in slides" :key="index">
        <div class="w-full h-full">
          <div class="example-slide">{{ slide.content }}</div>
        </div>
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </div>
</template>

<style>
.carousel-container {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
}

.example-slide {
  align-items: center;
  background-color: #666;
  color: #999;
  display: flex;
  font-size: 1.5rem;
  justify-content: center;
  min-height: 500px;
  width: 100%;
}

.carousel__prev,
.carousel__next {
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border-radius: 50%;
  padding: 10px;
}
</style>
