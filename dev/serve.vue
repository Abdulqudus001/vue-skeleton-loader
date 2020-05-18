<script>
import Vue from 'vue';
import { SkeletonLoaderVueSample } from '@/entry';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    SkeletonLoaderVueSample,
  }
});
</script>

<template>
  <div id="app">
    <skeleton-loader-vue-sample />
  </div>
</template>
