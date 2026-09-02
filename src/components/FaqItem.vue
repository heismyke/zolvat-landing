<script setup>
import { ref } from 'vue'
import { AnimatePresence, Motion } from 'motion-v'

defineProps({
  item: {
    type: Object,
    required: true,
  },
})

const isOpen = ref(false)
</script>

<template>
  <div class="border-b border-[#e6e6e6] py-6">
    <button
      type="button"
      class="flex w-full items-center justify-between gap-6 text-left text-xl text-[#202020]"
      @click="isOpen = !isOpen"
    >
      <span>{{ item.question }}</span>
      <Motion
        as="span"
        class="text-3xl leading-none text-[#008a57]"
        :animate="{ rotate: isOpen ? 45 : 0 }"
        :transition="{ duration: 0.2 }"
      >
        +
      </Motion>
    </button>

    <AnimatePresence>
      <Motion
        v-if="isOpen"
        as="div"
        :initial="{ height: 0, opacity: 0 }"
        :animate="{ height: 'auto', opacity: 1 }"
        :exit="{ height: 0, opacity: 0 }"
        :transition="{ duration: 0.28, ease: 'easeOut' }"
        class="overflow-hidden"
      >
        <p class="max-w-[680px] pt-5 text-base leading-7 text-[#737373]">
          {{ item.answer }}
        </p>
      </Motion>
    </AnimatePresence>
  </div>
</template>
