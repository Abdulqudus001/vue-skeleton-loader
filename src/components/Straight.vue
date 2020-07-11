<template>
  <div class="loader" :style="style" :class="bindClass"></div>
</template>

<script>
export default {
  props: {
    height: {
      type: [Number, String],
      default: 100
    },
    width: {
      type: [Number, String],
      default: 200
    },
    color: {
      type: String,
      default: 'rgba(0, 0, 0, 0.12)'
    },
    animation: {
      type: String,
      default: 'wave'
    },
    type: {
      type: String,
      default: 'rect',
    },
    rounded: {
      type: Boolean,
      default: false,
    },
    radius: {
      type: [Number, String],
      default: 0,
    }
  },
  computed: {
    style() {
      return {
        width: `${this.width}px`,
        height: `${this.height}px`,
        'background-color': `${this.color}`,
        'border-radius': this.rounded ? `${this.radius}px` : 0
      }
    },
    bindClass() {
      return `animation--${this.animation} shape--${this.type} shape--${this.rounded ? 'round': 'flat'}`;
    },
  }
};
</script>

<style scoped>
.loader {
  overflow: hidden;
  /* width: 100px;
  height: 100px; */
  position: relative;
}

.loader::before {
  content: "";
  display: block;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
}

/* Shape stylings */
.shape--text {
  height: 20px;
}

.shape--round {
  border-radius: 8px;
}
</style>