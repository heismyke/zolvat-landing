<script setup>
import { Motion } from 'motion-v'

defineProps({
  feature: {
    type: Object,
    required: true,
  },
})

const featureIcons = {
  1: '/tick-double-04.svg',
  2: '/money-send-circle.svg',
  3: '/Vector.png',
  4: '/Vector (1).png',
}
</script>

<template>
  <Motion
    as="article"
    class="flex min-h-[260px] flex-col justify-end rounded-lg bg-[#1b1b1b] p-8 text-white sm:min-h-[310px] sm:p-10"
    :whileHover="{ y: -6 }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-12">
      <img
        :src="featureIcons[feature.id]"
        :alt="`${feature.features_header} icon`"
        class="h-12 w-12 object-contain"
      />
    </div>

    <h3 class="brand-heading max-w-[330px] text-white">
      {{ feature.features_header }}
    </h3>
    <p class="brand-copy mt-4 text-left text-[#b9b9b9]">
      {{ feature.features_paragraph }}
    </p>
  </Motion>
</template>
