<script setup>
import { Motion } from 'motion-v'

defineProps({
  as: {
    type: String,
    default: 'div',
  },
  delay: {
    type: Number,
    default: 0,
  },
})
</script>

<template>
  <Motion
    :as="as"
    :initial="{ opacity: 0, y: 28 }"
    :whileInView="{ opacity: 1, y: 0 }"
    :inViewOptions="{ once: true, margin: '-80px' }"
    :transition="{ duration: 0.55, ease: 'easeOut', delay }"
  >
    <slot />
  </Motion>
</template>
