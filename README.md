# skeleton-loader-vue

> Loader showing skeleton view while data is being loaded to improve UX.

![Sample loader](https://res.cloudinary.com/ibnabubakre/image/upload/v1594505356/loader.gif)

---

## :cd: Install

* npm: `npm install skeleton-loader-vue --save`
* yarn: `yarn add skeleton-loader-vue`

## :rocket: Usage
You can import and register the component globally in your main.js, or import and use it in a particular component.

**To register in your `main.js`**
```javascript
import Vue from 'vue';
// Import the component
import VueSkeletonLoader from 'skeleton-loader-vue';

// Register the component globally
Vue.component('vue-skeleton-loader', VueSkeletonLoader);
```

**To register in your component**
```vue
<script>
import VueSkeletonLoader from 'skeleton-loader-vue'
export default {
  components: { VueSkeletonLoader },
};
</script>
```

Then you can use the component in your template

```vue
<template>
  <div>
    <skeleton-loader-vue
      type="circle"
      :width="200"
      :height="200"
      animation="fade"
    />
  </div>
</template>
```

## References

Types: circle, text, rect

Animations: fade, wave, pulse, pulse-x, pulse-y

Size: Overwrites the width and height with the provided value

Width: Sets width of loader

Height: Sets height of the loader

## Project setup

```shell
yarn install
```

### Compiles and hot-reloads for development

```shell
yarn serve
```

### Compiles and minifies for production

```shell
yarn build
```

### Lints and fixes files

```shell
yarn lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
