<script>
import Vue from 'vue';
import SkeletonLoaderVueSample from '@/entry';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    SkeletonLoaderVueSample,
  }
});
</script>

<template>
  <div id="app">
    <skeleton-loader-vue-sample type="circle" />
    <skeleton-loader-vue-sample type="rect" height="120" width="250" rounded radius="8" color="red" />
  </div>
</template>
