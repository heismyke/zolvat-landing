<script setup>
import { Motion } from 'motion-v'
</script>

<template>
  <header class="px-4 pt-4">
    <section
      class="relative min-h-[900px] overflow-hidden rounded-[32px] bg-linear-to-b from-white via-white to-[#DDF8FB]"
    >
      <!-- Hero Content -->
      <div
        class="relative z-10 mx-auto flex max-w-[900px] flex-col items-center pt-[110px] text-center"
      >
        <!-- Badge -->
        <Motion
          as="div"
          class="mb-5 rounded-full bg-[#F3F5FC] px-5 py-2 text-sm text-[#252525]"
          :initial="{ opacity: 0, y: 16 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.45, ease: 'easeOut' }"
        >
          Launch, Manage & Grow.
        </Motion>

        <!-- Heading -->
        <Motion
          as="h1"
          class="text-4xl leading-[1.05] font-semibold text-black sm:text-[56px]"
          :initial="{ opacity: 0, y: 22 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.55, ease: 'easeOut', delay: 0.08 }"
        >
          Modern Banking Built

          <span class="mt-2 block font-serif font-normal italic text-[#BFC9BD]">
            for modern businesses.
          </span>
        </Motion>

        <!-- Description -->
        <Motion
          as="p"
          class="mt-5 max-w-[600px] text-[16px] leading-6 text-[#828282]"
          :initial="{ opacity: 0, y: 18 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.5, ease: 'easeOut', delay: 0.16 }"
        >
          Power your business with secure accounts, seamless payments, and financial tools designed
          for growth.
        </Motion>

        <!-- Buttons -->
        <Motion
          as="div"
          class="mt-10 flex items-center gap-5"
          :initial="{ opacity: 0, y: 18 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.5, ease: 'easeOut', delay: 0.24 }"
        >
          <Motion
            as="button"
            class="rounded-full border border-[#A6A6A6] px-8 py-3 text-[16px] text-[#777] transition hover:bg-gray-100"
            :whileHover="{ y: -2 }"
            :whilePress="{ scale: 0.97 }"
          >
            Book a Demo
          </Motion>

          <Motion
            as="button"
            class="flex items-center gap-5 rounded-full bg-[#015130] px-8 py-3 text-[16px] text-white transition hover:bg-[#013d25]"
            :whileHover="{ y: -2 }"
            :whilePress="{ scale: 0.97 }"
          >
            Create an Account

            <span class="text-2xl leading-none"> → </span>
          </Motion>
        </Motion>
      </div>

      <!-- Hero Image -->
      <Motion
        as="div"
        class="absolute bottom-[-80px] left-1/2 w-full max-w-[950px] -translate-x-1/2"
        :initial="{ opacity: 0, y: 60, scale: 0.96 }"
        :animate="{ opacity: 1, y: 0, scale: 1 }"
        :transition="{ duration: 0.75, ease: 'easeOut', delay: 0.32 }"
      >
        <img src="/hero.png" alt="Zolvat banking application" class="w-full object-contain" />
      </Motion>
    </section>
  </header>
</template>
