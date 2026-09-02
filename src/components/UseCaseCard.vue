<script setup>
import { Motion } from 'motion-v'

defineProps({
  item: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <Motion
    as="article"
    :whileHover="{ y: -5 }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <img :src="item.image" :alt="item.title" class="aspect-[320/195] w-full rounded-lg object-cover" />
    <p class="mt-8 text-sm text-[#777]">{{ item.number }}</p>
    <h3 class="brand-heading mt-3 text-[#2b2b2b]">{{ item.title }}</h3>
    <ul class="mt-2 list-disc space-y-1 pl-5 text-base leading-7 text-[#626262]">
      <li v-for="point in item.points" :key="point">{{ point }}</li>
    </ul>
  </Motion>
</template>
