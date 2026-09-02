<script setup>
import { Motion } from 'motion-v'

defineProps({
  feature: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <Motion
    as="article"
    class="flex min-h-[260px] flex-col justify-end rounded-lg bg-[#1b1b1b] p-8 text-white sm:min-h-[310px] sm:p-10"
    :whileHover="{ y: -6 }"
    :transition="{ duration: 0.22, ease: 'easeOut' }"
  >
    <div class="mb-12 text-[#25c86a]">
      <svg
        v-if="feature.id === 1"
        class="h-12 w-12"
        viewBox="0 0 48 48"
        fill="none"
        aria-hidden="true"
      >
        <path d="M9 26.5l8 8L38 14" stroke="currentColor" stroke-width="6" stroke-linecap="round" stroke-linejoin="round" />
        <path d="M6 30l5 5M19 23l5 5" stroke="currentColor" stroke-width="5" stroke-linecap="round" />
      </svg>
      <svg
        v-else-if="feature.id === 2"
        class="h-14 w-14"
        viewBox="0 0 48 48"
        fill="none"
        aria-hidden="true"
      >
        <path d="M24 40c8.8 0 16-7.2 16-16S32.8 8 24 8 8 15.2 8 24s7.2 16 16 16Z" stroke="currentColor" stroke-width="4" />
        <path d="M24 15v18M18 29c1.4 2 3.4 3 6 3 3.2 0 5.4-1.6 5.4-4.2 0-2.8-2.4-3.6-5.4-4.4-3-.8-5-1.8-5-4.3 0-2.4 2.1-4.1 5-4.1 2.2 0 4 .8 5.2 2.4" stroke="currentColor" stroke-width="3" stroke-linecap="round" />
        <path d="M35 6h7v7" stroke="currentColor" stroke-width="4" stroke-linecap="round" stroke-linejoin="round" />
      </svg>
      <svg
        v-else-if="feature.id === 3"
        class="h-12 w-12"
        viewBox="0 0 48 48"
        fill="none"
        aria-hidden="true"
      >
        <path d="M24 42c9.4 0 17-7.6 17-17S33.4 8 24 8 7 15.6 7 25s7.6 17 17 17Z" fill="currentColor" />
        <path d="M17 24l5 5 10-12" stroke="#101010" stroke-width="4" stroke-linecap="round" stroke-linejoin="round" />
        <path d="M13 6l-5 5M35 6l5 5" stroke="currentColor" stroke-width="4" stroke-linecap="round" />
      </svg>
      <svg
        v-else
        class="h-12 w-12"
        viewBox="0 0 48 48"
        fill="none"
        aria-hidden="true"
      >
        <path d="M24 5 40 12v12c0 10-6.7 16.8-16 19-9.3-2.2-16-9-16-19V12l16-7Z" fill="currentColor" />
        <path d="M18 23h12v10H18V23Z" fill="#101010" />
        <path d="M21 23v-4a3 3 0 0 1 6 0v4" stroke="#101010" stroke-width="3" stroke-linecap="round" />
      </svg>
    </div>

    <h3 class="max-w-[280px] text-2xl leading-tight font-bold text-white">
      {{ feature.features_header }}
    </h3>
    <p class="mt-4 text-[15px] leading-6 text-[#b9b9b9]">
      {{ feature.features_paragraph }}
    </p>
  </Motion>
</template>
