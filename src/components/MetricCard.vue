<script setup>
import { Motion } from 'motion-v'

defineProps({
  metric: {
    type: Object,
    required: true,
  },
})

const metricIcons = {
  1: '/Margin.png',
  2: '/Margin (1).png',
  3: '/global.png',
}
</script>

<template>
  <Motion
    as="article"
    class="rounded-lg border border-[#e5e5e5] bg-white p-8"
    :whileHover="{ y: -5, boxShadow: '0 18px 45px rgba(0,0,0,0.08)' }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-9">
      <img
        :src="metricIcons[metric.id]"
        :alt="`${metric.metric_text} icon`"
        class="h-8 w-8 object-contain"
      />
    </div>

    <p class="text-2xl font-medium text-[#262626]">{{ metric.metrics_figure }}</p>
    <p class="mt-3 text-sm text-[#6d6d6d]">{{ metric.metric_text }}</p>
  </Motion>
</template>
