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
    <skeleton-loader-vue-sample type="circle" color="purple" class="my-loader" wave-color="green" />
    <skeleton-loader-vue-sample type="rect" height="120px" width="250px" rounded radius="8" color="red" wave-color="blue" />
  </div>
</template>
