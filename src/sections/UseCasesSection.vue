<script setup>
import MotionReveal from '@/components/MotionReveal.vue'
import UseCaseCard from '@/components/UseCaseCard.vue'
import { useCases } from '@/data/useCases'
</script>

<template>
  <section id="solutions" class="bg-[#fbfdfc] px-5 py-28 lg:py-36">
    <div class="mx-auto max-w-[1040px]">
      <MotionReveal>
      <h2 class="max-w-[760px] text-2xl leading-snug text-[#1f1f1f] sm:text-3xl lg:text-[34px]">
        Who can use Zolvat?
        <span class="rounded-md bg-[#ececec] px-1.5 text-[#8a8a8a]">Small-scaled businesses</span>
        <sup class="text-xs text-[#555]">01</sup>
        <span class="rounded-md bg-[#ececec] px-1.5 text-[#8a8a8a]">Medium-scaled businesses</span>
        <sup class="text-xs text-[#555]">02</sup>
        <span class="rounded-md bg-[#ececec] px-1.5 text-[#8a8a8a]">Large-scaled businesses</span>
        <sup class="text-xs text-[#555]">03</sup>
      </h2>
      </MotionReveal>

      <MotionReveal class="mt-24 grid gap-10 md:grid-cols-3" :delay="0.08">
        <UseCaseCard v-for="item in useCases" :key="item.number" :item="item" />
      </MotionReveal>
    </div>
  </section>
</template>
