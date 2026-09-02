<script setup>
import { ref } from 'vue'
import { faBars } from '@fortawesome/free-solid-svg-icons'
import { Navigation } from '../data/navbar'

const isMenuOpen = ref(false)
</script>

<template>
  <div class="border-b border-[#00000020]">
    <nav
      v-for="navigation in Navigation"
      :key="navigation.logo"
      class="mx-auto flex w-full max-w-[1200px] items-center justify-between px-4 py-4 sm:px-6 lg:px-8"
    >
      <!-- Logo -->
      <img :src="navigation.logo" alt="Zolvat logo" class="w-[110px]" />

      <!-- Desktop links -->
      <div class="hidden items-center gap-8 md:flex">
        <RouterLink
          v-for="item in navigation.nav_items.slice(0, -2)"
          :key="item.label"
          :to="item.href"
          class="font-avenir text-[14px] leading-none font-[450] text-[#737373]"
        >
          {{ item.label }}
        </RouterLink>
      </div>

      <!-- Desktop login -->
      <button class="font-avenir hidden rounded-full bg-[#252228] px-5 py-2 text-[14px] leading-none font-[450] text-white md:block">Login</button>

      <!-- Mobile hamburger -->
      <button
        @click="isMenuOpen = !isMenuOpen"
        class="flex h-10 w-10 items-center justify-center rounded-full border border-gray-300 md:hidden"
      >
        <FontAwesomeIcon :icon="faBars" class="h-5 w-5" />
      </button>
    </nav>

    <!-- Mobile Menu -->
    <div v-if="isMenuOpen" class="border-t border-[#00000020] bg-white px-5 py-5 md:hidden">
      <div v-for="navigation in Navigation" :key="navigation.logo" class="flex flex-col gap-4">
        <RouterLink
          v-for="item in navigation.nav_items.slice(0, -2)"
          :key="item.label"
          :to="item.href"
          class="font-avenir text-[14px] leading-none font-[450] text-[#737373]"
          @click="isMenuOpen = false"
        >
          {{ item.label }}
        </RouterLink>

        <button class="font-avenir mt-2 w-full rounded-full bg-[#252228] px-5 py-3 text-[14px] leading-none font-[450] text-white">Login</button>
      </div>
    </div>
  </div>
</template>
