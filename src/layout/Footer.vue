<script setup>
import { Navigation } from '@/data/navbar'
import {
  faDiscord,
  faGithub,
  faInstagram,
  faLinkedin,
  faTiktok,
  faXTwitter,
} from '@fortawesome/free-brands-svg-icons'

const excludedIndexes = [2, 4]
const socialLinks = [
  { label: 'X', href: '#x', icon: faXTwitter },
  { label: 'Instagram', href: '#instagram', icon: faInstagram },
  { label: 'TikTok', href: '#tiktok', icon: faTiktok },
  { label: 'LinkedIn', href: '#linkedin', icon: faLinkedin },
  { label: 'Discord', href: '#discord', icon: faDiscord },
  { label: 'GitHub', href: '#github', icon: faGithub },
]
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
    <div class="mt-5 grid gap-8 sm:grid-cols-[1fr_auto] sm:items-start">
      <div class="font-avenir max-w-[900px] space-y-2 text-[12px] leading-5 font-light text-[#737373]">
        <p>Copyright © 2026 Zolvat, LTD. All rights reserved.</p>

        <p>
          ZOLVAT LTD is authorized as an Electronic Money Institution (EMI) by the Central Bank of
          Cyprus (license № 115.1.3.59).
        </p>
      </div>

      <div class="flex items-center gap-8 text-[#b8b8b8]">
        <a
          v-for="social in socialLinks"
          :key="social.label"
          :href="social.href"
          :aria-label="social.label"
          class="text-2xl transition hover:text-[#008a57]"
        >
          <FontAwesomeIcon :icon="social.icon" />
        </a>
      </div>
    </div>

    <!-- Footer Image -->
    <div class="mt-10 overflow-hidden sm:mt-14 lg:mt-[60px]">
      <img src="/footer.png" alt="" class="w-full object-contain" />
    </div>
  </footer>
</template>
