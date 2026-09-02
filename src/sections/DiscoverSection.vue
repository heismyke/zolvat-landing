<script setup>
import FeatureCard from '@/components/FeatureCard.vue'
import MotionReveal from '@/components/MotionReveal.vue'
import { Features } from '@/data/features'
</script>

<template>
  <section id="products" class="px-5">
    <div class="mx-auto max-w-[1440px] rounded-[28px] bg-[#101010] px-5 py-24 text-white sm:rounded-[32px] sm:px-10 lg:px-0 lg:py-28">
      <MotionReveal class="mx-auto max-w-[980px] text-center">
        <h2 class="brand-heading text-white">
          Discover
          <span class="font-ibm-plex-serif font-medium italic tracking-[-0.022em] text-[#00d982]">
            zolvat
          </span>
        </h2>
        <p class="brand-copy mt-3 text-[#adadad]">Accounts and payments, made simple.</p>
        <div class="mt-8 flex justify-center gap-4">
          <button class="rounded-full bg-white px-7 py-3 text-base text-[#222]">Get Started</button>
          <button class="rounded-full bg-[#272727] px-7 py-3 text-base text-white">Learn More</button>
        </div>
      </MotionReveal>

      <MotionReveal class="relative mx-auto mt-20 max-w-[980px]" :delay="0.08">
        <img
          src="/Accounts _ User VISA MASTERCARD Merchant Onboarding_ Business Activities.png"
          alt="Zolvat dashboard"
          class="relative z-10 mx-auto w-full rounded-lg object-contain shadow-[0_0_100px_rgba(0,115,90,0.24)]"
        />
      </MotionReveal>

      <MotionReveal class="mx-auto mt-16 grid max-w-[980px] gap-8 md:mt-24 lg:grid-cols-[1fr_auto] lg:items-start">
        <div>
          <h2 class="discover-heading text-white">Experience seamless usability.</h2>
          <p class="discover-copy mt-4 max-w-[650px] text-[#adadad] md:mt-5 lg:text-left">
            Access a comprehensive marketplace offering IBANs, debit cards, payroll management,
            seamless payouts, and more, streamlining your financial operations and enhancing
            efficiency.
          </p>
        </div>
        <button class="w-max rounded-full bg-[#292929] px-7 py-3 text-base text-white">Learn More</button>
      </MotionReveal>

      <MotionReveal class="mx-auto mt-14 grid max-w-[860px] gap-6 md:mt-20 md:grid-cols-2 md:gap-8">
        <FeatureCard v-for="feature in Features" :key="feature.id" :feature="feature" />
      </MotionReveal>
    </div>
  </section>
</template>
