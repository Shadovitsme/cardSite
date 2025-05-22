<script setup>
import { reviewArray } from '@/dataArrays/reviewArray'

const props = defineProps({
  index: {
    type: Number,
    required: true,
  },
})
</script>
<template>
  <div class="flex gap-x-4 w-[900px]">
    <img class="shrink-0" src="/src/assets/images/quote.svg " />
    <div class="">
      <p class="font-light text-base text-[#EC6665] uppercase">
        {{ reviewArray[props.index].title }}
      </p>
      <p class="text-[#9D9D9D] font-light text-sm/18">{{ reviewArray[props.index].serve }}</p>
      <p class="text-[#3A3A3A] text-sm/22">{{ reviewArray[props.index].review }}</p>
    </div>
  </div>
</template>
