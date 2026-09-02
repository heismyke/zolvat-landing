<script setup>
import BrandLogo from '@/components/BrandLogo.vue'
import MotionReveal from '@/components/MotionReveal.vue'
import { trustLogos } from '@/data/trustLogos'
</script>

<template>
  <section class="mx-auto flex w-full max-w-[980px] flex-wrap items-center justify-center gap-x-10 gap-y-5 px-5 py-24">
    <MotionReveal class="contents">
      <span class="rounded-full border border-[#ececec] px-4 py-1.5 text-xs text-[#a0a0a0]">
        Trusted and funded by
      </span>
      <BrandLogo v-for="logo in trustLogos" :key="logo" :name="logo" />
    </MotionReveal>
  </section>
</template>
