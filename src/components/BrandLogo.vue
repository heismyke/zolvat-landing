<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <span class="text-sm font-medium text-[#6f6f6f] opacity-70 grayscale sm:text-base">
    {{ name }}
  </span>
</template>
