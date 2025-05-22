<script setup>
import { ref } from 'vue'

let imgUrlArray = [
  'src/assets/images/bgImg/wallpapersden.com_fantasy-castle-hd-landscape-art_1366x768.jpg',
  'src/assets/images/bgImg/i.webp',
  'src/assets/images/bgImg/132057-Oregon-mountains-hills-sunset-flowers-artwork-nature-landscape.jpg',
  'src/assets/images/bgImg/2.webp',
  'src/assets/images/bgImg/remembering-digital-art-landscape-5k-s1-1366x768.jpg',
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
        <p class="w-full text-center text-white text-[26px]">
          Гиды, Экскурсии и Туры по фентезийным мирам
        </p>
        <p class="w-full font-light text-center text-white text-sm">
          Частные гиды, индивидуальные экскурсии и туры по Магической академии, Летающему архипелагу
          и<br />
          другим фентезийным мирам
        </p>
      </div>
    </div>
  </div>
</template>
