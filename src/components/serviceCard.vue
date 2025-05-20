<script setup>
const props = defineProps({
  img: {
    type: String,
    required: true,
  },
  head: {
    type: String,
    required: true,
  },
})
</script>
<template>
  <div class="relative flex h-64 overflow-hidden rounded-xl hover:scale-110 duration-300">
    <div class="w-full overflow-hidden h-52">
      <img :src="props.img" class="w-full shrink-0" />
    </div>
    <div class="absolute bottom-2 w-full flex justify-center">
      <div class="bg-white p-2 w-full mx-5 rounded-sm shadow-gray-100 shadow-lg">
        <p class="w-full text-center text-[#333333] text-14/22 underline uppercase font-bold">
          {{ props.head }}
        </p>
      </div>
    </div>
  </div>
</template>
