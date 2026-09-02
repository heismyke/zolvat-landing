<script setup>
import { Motion } from 'motion-v'
import { faCheckDouble, faCircleDollarToSlot, faShieldHalved, faStopwatch } from '@fortawesome/free-solid-svg-icons'

defineProps({
  feature: {
    type: Object,
    required: true,
  },
})

const featureIcons = {
  1: faCheckDouble,
  2: faCircleDollarToSlot,
  3: faStopwatch,
  4: faShieldHalved,
}
</script>

<template>
  <Motion
    as="article"
    class="flex min-h-[260px] flex-col justify-end rounded-lg bg-[#1b1b1b] p-8 text-white sm:min-h-[310px] sm:p-10"
    :whileHover="{ y: -6 }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-12 text-[#25c86a]">
      <FontAwesomeIcon :icon="featureIcons[feature.id]" class="h-12 w-12" />
    </div>

    <h3 class="brand-heading max-w-[330px] text-white">
      {{ feature.features_header }}
    </h3>
    <p class="brand-copy mt-4 text-left text-[#b9b9b9]">
      {{ feature.features_paragraph }}
    </p>
  </Motion>
</template>
