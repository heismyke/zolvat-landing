<script setup>
import { Motion } from 'motion-v'
</script>

<template>
  <header class="px-2 pt-2 sm:px-4 sm:pt-4">
    <section
      class="relative min-h-[820px] overflow-hidden rounded-[24px] bg-linear-to-b from-white via-white to-[#DDF8FB] sm:min-h-[840px] sm:rounded-[32px] lg:min-h-[900px]"
    >
      <!-- Hero Content -->
      <div
        class="relative z-10 mx-auto flex max-w-[900px] flex-col items-center px-4 pt-20 text-center sm:pt-[110px]"
      >
        <!-- Badge -->
        <Motion
          as="div"
          class="mb-5 rounded-full bg-[#F3F5FC] px-5 py-2 text-sm text-[#252525] sm:text-[15px]"
          :initial="{ opacity: 0, y: 16 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.45, ease: 'easeOut' }"
        >
          Launch, Manage & Grow.
        </Motion>

        <!-- Heading -->
        <Motion
          as="h1"
          class="max-w-[760px] text-[38px] leading-[1.06] font-semibold text-black sm:text-[56px]"
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
          class="mt-5 max-w-[620px] text-lg leading-7 text-[#828282] sm:text-[16px] sm:leading-6"
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
          class="mt-9 grid w-full max-w-[410px] grid-cols-2 items-center gap-4 sm:mt-10 sm:flex sm:w-auto sm:max-w-none sm:gap-5"
          :initial="{ opacity: 0, y: 18 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.5, ease: 'easeOut', delay: 0.24 }"
        >
          <Motion
            as="button"
            class="min-h-16 rounded-full border border-[#A6A6A6] px-5 py-3 text-base text-[#777] transition hover:bg-gray-100 sm:min-h-0 sm:px-8 sm:text-[16px]"
            :whileHover="{ y: -2 }"
            :whilePress="{ scale: 0.97 }"
          >
            Book a Demo
          </Motion>

          <Motion
            as="button"
            class="flex min-h-16 items-center justify-center gap-4 rounded-full bg-[#015130] px-5 py-3 text-base text-white transition hover:bg-[#013d25] sm:min-h-0 sm:gap-5 sm:px-8 sm:text-[16px]"
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
        class="absolute bottom-[-18px] left-1/2 w-[145%] max-w-[700px] -translate-x-1/2 sm:bottom-[-55px] sm:w-full sm:max-w-[950px] lg:bottom-[-80px]"
        :initial="{ opacity: 0, y: 60, scale: 0.96 }"
        :animate="{ opacity: 1, y: 0, scale: 1 }"
        :transition="{ duration: 0.75, ease: 'easeOut', delay: 0.32 }"
      >
        <img src="/hero.png" alt="Zolvat banking application" class="w-full object-contain" />
      </Motion>
    </section>
  </header>
</template>
