<template>
  <span :style="btnStyles"><slot></slot></span>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "#f5487fff"
    },
  },
  computed: {
    btnStyles() {
      return {
        color: this.color,
      };
    }
  }
};
</script>