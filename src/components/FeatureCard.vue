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
    class="flex min-h-[250px] flex-col justify-end rounded-lg bg-[#1b1b1b] p-6 text-white sm:min-h-[290px] sm:p-8 lg:min-h-[310px] lg:p-10"
    :whileHover="{ y: -6 }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-8 md:mb-12">
      <img
        :src="featureIcons[feature.id]"
        :alt="`${feature.features_header} icon`"
        class="h-10 w-10 object-contain md:h-12 md:w-12"
      />
    </div>

    <h3 class="feature-card-heading max-w-[330px] text-white">
      {{ feature.features_header }}
    </h3>
    <p class="feature-card-copy mt-3 text-left text-[#b9b9b9] md:mt-4">
      {{ feature.features_paragraph }}
    </p>
  </Motion>
</template>
