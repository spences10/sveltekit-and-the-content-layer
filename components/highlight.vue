<template>
  <span :style="spanStyles"><slot></slot></span>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: '#f5487fff',
    },
  },
  computed: {
    spanStyles() {
      return {
        color: this.color,
      }
    },
  },
}
</script>
