# skeleton-loader-vue

> Loader showing skeleton view while data is being loaded to improve UX.

![Sample loader](https://res.cloudinary.com/ibnabubakre/image/upload/v1594505356/loader.gif)

---

## :cd: Installation

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
import VueSkeletonLoader from 'skeleton-loader-vue';
export default {
  components: { VueSkeletonLoader },
};
</script>
```

**Using loader in your `.vue` file**

```vue
<template>
  <div class="facebook-card">
    <skeleton-loader-vue
      type="circle"
      :width="200"
      :height="200"
      animation="fade"
    />
  </div>
</template>
```

This would give create a circle having a width and heigth of 200px and an animation of fade.

## API

### Props

|Prop|Type|Default|Options|Description|
|---|---|---|---|---|
|width|number, string|200||The is the width of the loader, and can be either a number or string. This property would be overridden if the `size` props is set|
|height|number, string|100||The is the height of the loader, and can be either a number or string. This property would be overridden if the `size` props is set|
|size|number,string|||This is used to give the loader the same width and height. The property would override the width and height previously set|
|type|string|'rect'|rect, circle|This is the type of the loader. It could be circle or rectangle shaped|
|animation|string|'wave'|fade, wave, pulse, pulse-x, pulse-y|The animation to be applied to the loader|
|color|string|rgba(0,0,0,0.12)||The sets the color of the loader. It accepts all valid CSS colors (rgb, hsl, hex included)|
|wave-color|string|rgba(0,0,0,0.12)||The sets the color of the wave. It accepts all valid CSS colors (rgb, hsl, hex included)|
|rounded|boolean|false||Add this prop to give a non-circle loader a border-radius 0f 8px|
|radius|number,string|8||This is used to determine the border radius of the loader|


## Project setup

### Install dependencies

* npm: `npm install`
* yarn: `yarn`

### Start Dev Server

* npm: `npm run serve`
* yarn: `yarn serve`

### Compiles and minifies for production

* npm: `npm run build`
* yarn: `yarn build`

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
