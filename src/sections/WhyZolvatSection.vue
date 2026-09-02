<script setup>
import { Motion } from 'motion-v'
import MotionReveal from '@/components/MotionReveal.vue'
</script>

<template>
  <section class="overflow-hidden bg-white py-20 lg:py-28">
    <div class="mx-auto grid max-w-[1440px] items-center gap-12 px-5 lg:grid-cols-2 lg:px-0">
      <MotionReveal class="mx-auto w-full max-w-[520px] lg:ml-auto">
        <h2 class="text-5xl font-semibold text-[#414141]">Why Zolvat?</h2>
        <div class="mt-28">
          <h3 class="max-w-[520px] text-2xl leading-tight font-semibold text-[#222]">
            Banking Built for Businesses That Operate Globally
          </h3>
          <p class="mt-6 max-w-[520px] text-base leading-7 text-[#777]">
            Zolvat combines banking, payments, compliance, and automation into one platform so your
            business can scale without financial friction.
          </p>
        </div>
        <div class="mt-28 grid gap-8 border-t border-[#eee] pt-8 text-sm leading-7 text-[#686868] sm:grid-cols-2">
          <p>Zolvat is for modern digital businesses.</p>
          <div class="grid gap-2">
            <p>Short & smooth onboarding.</p>
            <p>Fast international payments.</p>
            <p>Limitless integrations.</p>
            <p>No hidden fees.</p>
          </div>
        </div>
      </MotionReveal>

      <MotionReveal class="relative min-h-[560px]" :delay="0.08">
        <Motion
          as="img"
          src="/image 4.png"
          alt="Global payment network"
          class="absolute right-[-120px] top-1/2 h-[760px] max-w-none -translate-y-1/2 opacity-55"
          :initial="{ opacity: 0, x: 70, scale: 0.97 }"
          :whileInView="{ opacity: 0.55, x: 0, scale: 1 }"
          :animate="{ y: [0, -18, 0], scale: [1, 1.025, 1] }"
          :inViewOptions="{ once: true, margin: '-80px' }"
          :transition="{
            opacity: { duration: 0.7, ease: 'easeOut' },
            x: { duration: 0.7, ease: 'easeOut' },
            scale: { duration: 10, repeat: Infinity, ease: 'easeInOut' },
            y: { duration: 10, repeat: Infinity, ease: 'easeInOut' },
          }"
        />
      </MotionReveal>
    </div>
  </section>
</template>
