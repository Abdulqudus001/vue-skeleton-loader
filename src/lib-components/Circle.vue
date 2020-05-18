<template>
  <div class="circle-loader" :style="style" :class="bindClass"></div>
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
      default: 100
    },
    color: {
      type: String,
      default: 'rgba(0, 0, 0, 0.12)'
    },
    animation: {
      type: String,
      default: 'wave'
    }
  },
  computed: {
    style() {
      return `width: ${this.width}px; height: ${this.height}px; background-color: ${this.color}`;
    },
    bindClass() {
      return `animation--${this.animation}`;
    },
  }
};
</script>

<style scoped>
.circle-loader {
  overflow: hidden;
  width: 100px;
  height: 100px;
  background-color: red;
  border-radius: 50%;
  position: relative;
}

.circle-loader::before {
  content: "";
  display: block;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
}
</style>