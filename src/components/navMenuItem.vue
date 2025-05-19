<script setup>
const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  href: {
    type: String,
    required: false,
    default: '#',
  },
})
</script>
<template>
  <a :href="props.href">
    <p class="text-[#424242] text-sm uppercase">{{ props.label }}</p>
  </a>
</template>
