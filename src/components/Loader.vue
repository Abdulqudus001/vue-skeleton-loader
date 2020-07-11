<template>
  <div class="loader">
    <circle-loader
      v-if="type === 'circle'"
      :width="loaderWidth"
      :height="loaderHeight"
      :animation="animation"
    />
    <square-loader
      v-else
      :width="loaderWidth"
      :height="loaderHeight"
      :animation="animation"
      :type="type"
    />
  </div>
</template>

<script>
import CircleLoader from './Circle.vue';
import SquareLoader from './Straight.vue';

export default {
  components: {
    CircleLoader,
    SquareLoader
  },

  props: {
    type: {
      type: String,
      default: 'rect',
    },
    size: {
      type: [Number, String],
    },
    animation: {
      type: String,
      default: 'wave',
    },
    height: {
      type: [Number, String],
    },
    width: {
      type: [Number, String],
    },
    color: {
      type: String,
      default: 'rgba(0, 0, 0, 0.12)'
    },
  },
  computed: {
    loaderWidth() {
      if (this.size) {
        return this.size;
      } else {
        return this.width;
      }
    },
    loaderHeight() {
      if (this.size) {
        return this.size;
      } else {
        return this.height;
      }
    },
  },
};
</script>

<style>
.loader {
  width: fit-content;
  cursor: wait;
}

/* Animation definitions */
@keyframes fade {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0.4;
  }
  100% {
    opacity: 1;
  }
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(0.85);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes pulse-x {
  0% {
    transform: scaleX(1);
  }
  50% {
    transform: scaleX(0.75);
  }
  100% {
    transform: scaleX(1);
  }
}

@keyframes pulse-y {
  0% {
    transform: scaleY(1);
  }
  50% {
    transform: scaleY(0.75);
  }
  100% {
    transform: scaleY(1);
  }
}

@keyframes wave {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}

/* Animation classes */
.animation--fade {
  animation: fade 1.5s linear .5s infinite;
}

.animation--wave::before {
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.5),
    transparent
  );
  animation: wave 1.5s linear .5s infinite;
}

.animation--pulse-x {
  animation: pulse-x 1.5s linear .5s infinite;
}

.animation--pulse-y {
  animation: pulse-y 1.5s linear .5s infinite;
}

.animation--pulse {
  animation: pulse 1.5s linear .5s infinite;
}
</style>