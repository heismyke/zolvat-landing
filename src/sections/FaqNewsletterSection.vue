<script setup>
import FaqItem from '@/components/FaqItem.vue'
import MotionReveal from '@/components/MotionReveal.vue'
import { FrequentlyAskedQuestions } from '@/data/questions'
</script>

<template>
  <section id="support" class="border-t border-[#e9e9e9] bg-white px-5 py-24 lg:py-32">
    <MotionReveal class="mx-auto grid max-w-[1120px] gap-12 lg:grid-cols-[0.75fr_1.25fr]">
      <h2 class="text-5xl leading-tight font-normal text-[#242424]">
        Frequently<br />Asked<br /><span class="underline decoration-2 underline-offset-4">Questions</span>
      </h2>

      <div>
        <FaqItem
          v-for="item in FrequentlyAskedQuestions"
          :key="item.id"
          :item="item"
        />
        <RouterLink to="#resources" class="mt-8 inline-flex items-center gap-3 text-lg text-[#008a57]">
          Learn More Zolvat
          <span class="flex h-7 w-7 items-center justify-center rounded-full bg-[#dff5ef]">→</span>
        </RouterLink>
      </div>
    </MotionReveal>

    <MotionReveal as="form" class="mx-auto mt-40 max-w-[700px] text-center" :delay="0.08">
      <h2 class="text-3xl font-medium text-[#333]">Stay Updated</h2>
      <p class="mt-4 text-xl text-[#777]">Be the first to hear about news from our newsletters</p>
      <div class="mt-8 flex flex-col gap-4 sm:flex-row">
        <input
          type="email"
          placeholder="Email"
          class="min-h-14 flex-1 rounded-full bg-[#f4f4f4] px-7 text-lg outline-none placeholder:text-[#c4c4c4]"
        />
        <button class="min-h-14 rounded-full bg-black px-8 text-lg text-white">Notify Me</button>
      </div>
    </MotionReveal>
  </section>
</template>
