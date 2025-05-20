<script setup>
import HelloPic from './components/helloPic.vue'
import NavMenuItem from './components/navMenuItem.vue'
import ServiceCard from './components/serviceCard.vue'
import { dataServiceArray } from './dataArrays/dataServiceArray';
</script>

<template>
  <div
    class="absolute top-0 left-0 right-0 px-1.5 pb-3 flex justify-between border-b-2 border-yellow-400"
  >
    <img class="mt-3" src="./assets/images/logoSite.png" />
    <div class="my-auto gap-x-7 flex mr-4 h-full pt-5">
      <NavMenuItem label="ГЛАВНАЯ"></NavMenuItem>
      <NavMenuItem label="Услуги"></NavMenuItem>
      <NavMenuItem label="ПОЛЕЗНАЯ ИНФОРМАЦИЯ"></NavMenuItem>
      <NavMenuItem label="БЛОГ"></NavMenuItem>
      <NavMenuItem label="О НАС"></NavMenuItem>
    </div>
  </div>
  <div class="mt-[70px]"><HelloPic></HelloPic></div>
  <p class="uppercase text-[#424242] w-full text-center my-10 text-3xl">Наши услуги</p>
  <div class=" lg:mx-80 mx-10 flex justify-center">
    <div class="grid lg:grid-cols-4 grid-cols-1 md:grid-cols-2 gap-5 ">
      <ServiceCard v-for="item in dataServiceArray" :key="item" :head="item.head" :img="item.img"></ServiceCard>

    </div>
  </div>
</template>
