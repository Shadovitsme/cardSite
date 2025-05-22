<script setup>
import { Carousel, Slide, Navigation } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'
import ReviewComponent from './reviewComponent.vue'
import { reviewArray } from '@/dataArrays/reviewArray'
</script>

<template>
  <div class="carousel-container w-full flex justify-center">
    <Carousel class="w-[1000px]" :items-to-show="1" :wrap-around="true">
      <Slide v-for="(item, index) in reviewArray.length" :key="item">
        <ReviewComponent :index="index"></ReviewComponent>
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </div>
</template>

<style>
.carousel__prev,
.carousel__next {
  color: #ec6665;
  size: 40px;
}
</style>
