<script setup>
import { Navigation } from '@/data/navbar'

const excludedIndexes = [2, 4]
</script>

<template>
  <footer class="mx-auto w-full max-w-[1200px] px-5 sm:px-6 lg:px-8">
    <!-- Footer Navigation -->
    <div
      v-for="navigation in Navigation"
      :key="navigation.logo"
      class="grid grid-cols-2 gap-x-8 gap-y-10 border-y border-[#00000020] py-10 sm:grid-cols-3 lg:grid-cols-5 lg:gap-10 lg:py-14"
    >
      <div
        v-for="item in navigation.nav_items.filter((_, index) => !excludedIndexes.includes(index))"
        :key="item.label"
      >
        <!-- Heading -->
        <p class="mb-4 text-[14px] font-medium text-[#000000DF] sm:text-[15px]">
          {{ item.label }}
        </p>

        <!-- Links -->
        <div v-for="i in item.links" :key="i.label" class="mb-2">
          <RouterLink
            :to="i.href"
            class="block text-[14px] leading-6 text-[#00000072] transition hover:text-black sm:text-[15px]"
          >
            {{ i.label }}
          </RouterLink>
        </div>
      </div>
    </div>

    <!-- Legal Information -->
    <div class="mt-5 max-w-[900px] space-y-2 text-[10px] leading-5 text-[#00000072] sm:text-[11px]">
      <p>Copyright © 2026 Zolvat, LTD. All rights reserved.</p>

      <p>
        ZOLVAT LTD is authorized as an Electronic Money Institution (EMI) by the Central Bank of
        Cyprus (license № 115.1.3.59).
      </p>
    </div>

    <!-- Footer Image -->
    <div class="mt-10 overflow-hidden sm:mt-14 lg:mt-[60px]">
      <img src="/footer.png" alt="" class="w-full object-contain" />
    </div>
  </footer>
</template>
