<script setup>
import { ref } from 'vue'

let imgUrlArray = [
  'https://media.cntraveller.in/wp-content/uploads/2016/07/spaincoastaltownslead-1366x768.jpg',
  'https://www.fonstola.ru/pic/201308/1366x768/fonstola.ru_103637.jpg',
  'https://beoriginaltours.com/wp-content/uploads/2017/06/ian-kelsall-dXDHJ1wXEL0-unsplash.jpg',
  'https://s2.best-wallpaper.net/wallpaper/1366x768/1808/Valencia-Spain-city-houses-beach_1366x768.jpg',
  'https://www.zastavki.com/pictures/1366x768/2017World___Spain_View_of_the_city_of_Cadaques__Costa_Brava._Spain_113073_24.jpg',
]
let srAddr = ref(imgUrlArray[0])

function changeImageRandomly() {
  setInterval(() => {
    // Add more images to imgUrlArray if needed
    const randomIndex = Math.floor(Math.random() * imgUrlArray.length)
    srAddr.value = imgUrlArray[randomIndex]
  }, 3000) // change every 3 seconds
}

changeImageRandomly()
</script>

<template>
  <div class="w-full h-[450px] overflow-hidden">
    <div
      class="w-full h-full bg-center bg-cover flex items-center justify-center duration-700"
      :style="{ backgroundImage: `url('${srAddr}')` }"
    >
      <div class="bg-opacity-80 bg-[#EC6665] py-[30px] px-4">
        <p class="w-full text-center text-white text-[26px]">Гиды, Экскурсии и Туры по Испании</p>
        <p class="w-full font-light text-center text-white text-sm">
          Частные гиды, индивидуальные экскурсии и туры по Андалусии, Мадриду и<br />
          другим регионам Испании
        </p>
      </div>
    </div>
  </div>
</template>
