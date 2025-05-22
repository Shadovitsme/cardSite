<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  body: {
    type: String,
    required: true,
  },
  img: {
    type: String,
    required: true,
  },
})
</script>
<template>
  <div class="w-52">
    <div class="w-full flex justify-center">
      <img class="size-16" :src="props.img" />
    </div>

    <p class="w-full my-3 text-center uppercase text-[#333333]">{{ props.title }}</p>
    <p class="w-full text-center text-[#9D9D9D]">{{ props.body }}</p>
  </div>
</template>
