<script setup>
const data = [
  '<div class="h-10 w-10 bg-red-100">Slide 1</div>',
  '<div class="example-slide">Slide 2</div>',
  '<div class="example-slide">Slide 3</div>',
]
</script>

<template>
  <vue-carousel :data="data" :controls="true"></vue-carousel>
</template>

<style>
.example-slide {
  align-items: center;
  background-color: #666;
  color: #999;
  display: flex;
  font-size: 1.5rem;
  justify-content: center;
  min-height: 500px;
  width: 110px;
}
</style>
