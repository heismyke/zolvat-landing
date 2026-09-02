<script setup>
import MotionReveal from '@/components/MotionReveal.vue'
</script>

<template>
  <section id="resources" class="px-5 py-28 lg:py-36">
    <div class="mx-auto max-w-[1180px] text-center">
      <MotionReveal>
      <h2 class="brand-heading mx-auto max-w-[760px] text-[#bebebe]">
        What people have to say about
        <span class="text-black">ZOLVAT</span>
      </h2>
      <p class="brand-copy mx-auto mt-5 max-w-[650px] text-[#777]">
        Six years of uninterrupted operation. Trillions deposited. Independently audited, onchain,
        and open to verify.
      </p>
      </MotionReveal>

      <MotionReveal class="relative mx-auto mt-24 max-w-[980px]" :delay="0.08">
        <div class="absolute inset-x-[-80px] top-0 hidden h-full rounded-2xl bg-white shadow-[0_20px_70px_rgba(0,0,0,0.04)] lg:block"></div>
        <article class="relative overflow-hidden rounded-2xl border border-[#efefef] bg-white px-7 py-24 shadow-[0_22px_80px_rgba(0,0,0,0.03)] sm:px-14 lg:px-28">
          <div class="pointer-events-none absolute inset-0 opacity-40">
            <div class="absolute left-[9%] top-[-30%] h-[160%] w-[28%] rounded-full border border-[#e9e9e9]"></div>
            <div class="absolute inset-y-0 left-[21%] w-px rotate-[-52deg] bg-[#eeeeee]"></div>
            <div class="absolute inset-y-0 right-[30%] w-px rotate-[54deg] bg-[#eeeeee]"></div>
          </div>
          <blockquote class="relative mx-auto max-w-[700px] font-serif text-3xl leading-tight text-black sm:text-4xl">
            “Every hour spent chasing bugs is time away from building features that users actually
            want. Interfere gives your team time to focus on what actually matters.”
          </blockquote>
          <div class="relative mt-14 flex items-center justify-center gap-4">
            <div class="flex h-12 w-12 items-center justify-center rounded-full bg-[#111] text-sm font-semibold text-white">
              DB
            </div>
            <div class="text-left">
              <p class="text-base text-[#303030]">Dylan Babbs</p>
              <p class="text-sm text-[#777]">CTO of Profound</p>
            </div>
          </div>
        </article>
      </MotionReveal>
    </div>
  </section>
</template>
