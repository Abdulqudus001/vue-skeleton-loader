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
    <!-- <skeleton-loader-vue-sample type="text" height="12" width="250" rounded radius="8" color="red" /> -->
  </div>
</template>
