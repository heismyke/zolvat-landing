<script setup>
import { Motion } from 'motion-v'
import { faArrowsRotate, faCircleNodes, faGlobe } from '@fortawesome/free-solid-svg-icons'

defineProps({
  metric: {
    type: Object,
    required: true,
  },
})

const metricIcons = {
  1: faArrowsRotate,
  2: faCircleNodes,
  3: faGlobe,
}
</script>

<template>
  <Motion
    as="article"
    class="rounded-lg border border-[#e5e5e5] bg-white p-8"
    :whileHover="{ y: -5, boxShadow: '0 18px 45px rgba(0,0,0,0.08)' }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-9 text-[#008a57]">
      <FontAwesomeIcon :icon="metricIcons[metric.id]" class="h-6 w-6" />
    </div>

    <p class="text-2xl font-medium text-[#262626]">{{ metric.metrics_figure }}</p>
    <p class="mt-3 text-sm text-[#6d6d6d]">{{ metric.metric_text }}</p>
  </Motion>
</template>
