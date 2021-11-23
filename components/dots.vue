<template>
  <div :style="btnStyles"/>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "#10183e"
    },
    bgColor: {
      type: String,
      default: "#121212"
    },
  },
  computed: {
    btnStyles() {
      return {
        position: "absolute",
        right: "0",
        top: "0",
        width: "6.7vw",
        height: "100vh",
        "background-image": `radial-gradient(${this.color} 20%, ${this.bgColor} 20%)`,
        "background-size": "25px 25px",
      };
    }
  }
};
</script>