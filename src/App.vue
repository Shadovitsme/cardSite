<script setup>
import CarouselComponent from './components/carouselComponent.vue'
import HelloPic from './components/helloPic.vue'
import NavMenuItem from './components/navMenuItem.vue'
import ServiceCard from './components/serviceCard.vue'
import WhyWe from './components/whyWe.vue'
import { dataServiceArray } from './dataArrays/dataServiceArray'
import { whyWeArray } from './dataArrays/whyWeArray'
</script>

<template>
  <div
    class="absolute top-0 left-0 right-0 px-1.5 pb-3 flex justify-between border-b-2 border-yellow-400"
  >
    <img class="mt-3 size-11 my-auto" src="./assets/images/logoSite.jpg" />
    <div class="my-auto gap-x-7 flex mr-4 h-full pt-5">
      <NavMenuItem label="ГЛАВНАЯ"></NavMenuItem>
      <NavMenuItem label="Услуги"></NavMenuItem>
      <NavMenuItem label="ПОЛЕЗНАЯ ИНФОРМАЦИЯ"></NavMenuItem>
      <NavMenuItem label="БЛОГ"></NavMenuItem>
      <NavMenuItem label="О НАС"></NavMenuItem>
    </div>
  </div>
  <div class="mt-[70px]"><HelloPic></HelloPic></div>
  <div class="bg-[#FAFAFA] pt-10">
    <p class="uppercase text-[#424242] w-full text-center mb-10 text-3xl">Наши услуги</p>
    <div class="lg:px-80 px-10 flex justify-center pb-20">
      <div class="grid lg:grid-cols-4 grid-cols-1 md:grid-cols-2 gap-5">
        <ServiceCard
          v-for="item in dataServiceArray"
          :key="item"
          :head="item.head"
          :img="item.img"
        ></ServiceCard>
      </div>
    </div>
  </div>
  <div>
    <p class="uppercase text-[#424242] w-full text-center my-10 text-3xl">Почему мы?</p>
    <div class="flex justify-center w-full mb-10 space-x-3">
      <WhyWe
        v-for="item in whyWeArray"
        :key="item"
        :title="item.title"
        :body="item.content"
        :img="item.img"
      ></WhyWe>
    </div>
  </div>
  <!-- about us start -->
  <div class="bg-[#FAFAFA] pt-10 pb-5">
    <p class="uppercase text-[#424242] w-full text-center mb-10 text-3xl">О нас</p>
    <div class="flex justify-center w-full mb-10 space-x-6">
      <div class="h-full items-start">
        <img
          src="/src/assets/images/ownerPortrait.jpg"
          class="h-full max-h-[500px] w-auto object-contain shrink-0 rounded-lg"
        />
      </div>
      <div class="w-[512px]">
        <p class="text-[#5D5D5D]">
          Добрый день, уважаемые гости моего портала! Меня зовут Эльдар Вестарион. Я — магистр
          путеводных чар и организатор путешествий по фантастическим мирам. Работаю под знаменем
          "Звездный Путь Эфира" и предлагаю свои услуги для проведения экскурсий по магическим
          землям — от Лунных Равнин Эльмерии до Теневых Лесов Ксарона, от Огненных Пустошей
          Драконьего Пика до Сияющих Башен Аурелии (подробнее в разделе "Путешествия"). Я организую
          как прогулки с проводником в выбранных вами мирах, так и выездные экспедиции на крылатых
          грифонах или эфирных ладьях из вашего текущего измерения в земли приключений. Также я
          создаю авторские маршруты через Забытые Королевства, Кристальные Озера и другие уголки
          магических миров. В рамках услуг помогаю с приобретением заколдованных артефактов для
          входа в запретные зоны, выбором таверн и магических убежищ для отдыха, а также предлагаю
          услуги портального перехода между мирами.
        </p>
        <div class="mt-4 ml-10">
          <div class="p-1.5 bg-[#EC6665] w-fit rounded-sm">
            <p class="text-white font-light">Я говорю на:</p>
          </div>
          <ul class="mt-2">
            <li class="flex">
              <img src="/src/assets/images/good.svg" />
              <p class="text-[#5D5D5D] ml-1.5 font-light">Русском</p>
            </li>
            <li class="flex">
              <img src="/src/assets/images/good.svg" />
              <p class="text-[#5D5D5D] ml-1.5 font-light">Английском</p>
            </li>
            <li class="flex">
              <img src="/src/assets/images/good.svg" />
              <p class="text-[#5D5D5D] ml-1.5 font-light">Общем</p>
            </li>
            <li class="flex">
              <img src="/src/assets/images/good.svg" />
              <p class="text-[#5D5D5D] ml-1.5 font-light">Эльфийском</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  <!-- about us end -->
  <div class="mb-28">
    <p class="uppercase w-full text-center my-10 text-3xl">Отзывы</p>
    <div class="w-full justify-center flex items-center">
      <CarouselComponent></CarouselComponent>
    </div>
  </div>
</template>
