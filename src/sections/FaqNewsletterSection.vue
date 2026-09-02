<script setup>
import FaqItem from '@/components/FaqItem.vue'
import MotionReveal from '@/components/MotionReveal.vue'
import { FrequentlyAskedQuestions } from '@/data/questions'
</script>

<template>
  <section id="support" class="bg-white px-5 pb-24 lg:pb-32">
    <div class="-mx-5 overflow-hidden border-t border-[#e9e9e9]">
      <img
        src="/Gradient+Blur.png"
        alt=""
        class="mx-auto h-[170px] w-full max-w-[1330px] object-fill sm:h-[220px] lg:h-[289px]"
      />
    </div>

    <MotionReveal class="mx-auto mt-12 grid max-w-[1120px] gap-12 lg:mt-4 lg:grid-cols-[0.75fr_1.25fr]">
      <h2 class="brand-heading text-[#242424]">
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
      <h2 class="brand-heading text-[#333]">Stay Updated</h2>
      <p class="brand-copy mt-4 text-[#777]">Be the first to hear about news from our newsletters</p>
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
