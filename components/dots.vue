<template>
  <div :style="styles" />
</template>

<script>
export default {
  props: {
    width: {
      type: String,
      default: '10vw', // try 6.7vw if current too wide
    },
    rgColor: {
      type: String,
      default: '#10183e',
    },
    rgBgColor: {
      type: String,
      default: '#090E24',
    },
    rgColorSize: {
      type: String,
      default: '18%',
    },
    rgBgColorSize: {
      type: String,
      default: '20%',
    },
    bgSize: {
      type: String,
      default: '25px',
    },
  },

  computed: {
    styles() {
      return {
        position: 'absolute',
        right: '0',
        top: '0',
        width: `${this.width}`,
        height: '100vh',
        'background-image': `radial-gradient(${this.rgColor} ${this.rgColorSize}, ${this.rgBgColor} ${this.rgBgColorSize})`,
        'background-size': `${this.bgSize} ${this.bgSize}`,
      }
    },
  },
}
</script>
