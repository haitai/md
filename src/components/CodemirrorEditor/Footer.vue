<script setup lang="ts">
import { useStore } from '@/stores'

const store = useStore()
const { readingTime } = storeToRefs(store)
</script>

<template>
  <footer
    class="flex select-none items-center justify-end px-5 py-2 text-xs"
  >
    <div class="space-x-2">
      <span> {{ readingTime.words }} 个词 </span>
      <span> {{ readingTime.chars }} 个字符 </span>
      <span> 阅读大约需 {{ readingTime.minutes }} 分钟 </span>
    </div>
  </footer>
</template>
