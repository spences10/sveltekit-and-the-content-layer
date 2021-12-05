<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
})
</script>

<template>
  <div
    class="-mt-3 slidev-layout w-full h-full grid grid-cols-5 gap-10"
  >
    <div class="-ml-7 col-span-2 col-left" :class="props.class">
      <slot/>
    </div>
    <div class="-mr-7 col-span-3 col-right" :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>
