<script setup>
import { Motion } from 'motion-v'

defineProps({
  metric: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <Motion
    as="article"
    class="rounded-lg border border-[#e5e5e5] bg-white p-8"
    :whileHover="{ y: -5, boxShadow: '0 18px 45px rgba(0,0,0,0.08)' }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-9 text-[#008a57]">
      <svg
        v-if="metric.id === 1"
        class="h-6 w-6"
        viewBox="0 0 24 24"
        fill="none"
        aria-hidden="true"
      >
        <path d="M4 12a8 8 0 0 1 13.7-5.6M20 12A8 8 0 0 1 6.3 17.6" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
        <path d="M17 3v4h-4M7 21v-4h4" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
      </svg>
      <svg
        v-else-if="metric.id === 2"
        class="h-6 w-6"
        viewBox="0 0 24 24"
        fill="currentColor"
        aria-hidden="true"
      >
        <circle cx="7" cy="7" r="3" />
        <circle cx="17" cy="7" r="3" />
        <circle cx="7" cy="17" r="3" />
        <circle cx="17" cy="17" r="3" />
      </svg>
      <svg
        v-else
        class="h-6 w-6"
        viewBox="0 0 24 24"
        fill="none"
        aria-hidden="true"
      >
        <circle cx="12" cy="12" r="9" stroke="currentColor" stroke-width="1.8" />
        <path d="M3 12h18M12 3c2.5 2.6 3.8 5.6 3.8 9s-1.3 6.4-3.8 9c-2.5-2.6-3.8-5.6-3.8-9S9.5 5.6 12 3Z" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" />
      </svg>
    </div>

    <p class="text-2xl font-medium text-[#262626]">{{ metric.metrics_figure }}</p>
    <p class="mt-3 text-sm text-[#6d6d6d]">{{ metric.metric_text }}</p>
  </Motion>
</template>
