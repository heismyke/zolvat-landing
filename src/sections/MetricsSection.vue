<script setup>
import MetricCard from '@/components/MetricCard.vue'
import MotionReveal from '@/components/MotionReveal.vue'
import { metrics } from '@/data/metrics'
</script>

<template>
  <section class="px-5 py-20 lg:py-28">
    <div class="mx-auto max-w-[980px]">
      <MotionReveal class="grid gap-8 sm:grid-cols-[1fr_auto] sm:items-start">
        <div>
          <h2 class="brand-heading text-[#4a4a4a]">Metrics</h2>
          <p class="brand-copy mt-5 max-w-[520px] text-[#777] sm:text-left">
            Reach millions of users and access billions in capital with a few lines of code.
          </p>
        </div>
        <button class="w-max rounded-full bg-[#f1f1f1] px-7 py-3 text-base text-[#2d2d2d]">Learn More</button>
      </MotionReveal>

      <MotionReveal class="mt-20 grid gap-7 md:grid-cols-3" :delay="0.08">
        <MetricCard v-for="metric in metrics" :key="metric.id" :metric="metric" />
      </MotionReveal>
    </div>
  </section>
</template>
