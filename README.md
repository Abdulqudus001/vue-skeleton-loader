# skeleton-loader-vue

## Install

npm

```shell
npm install skeleton-loader-vue --save
```

yarn

```shell
yarn add skeleton-loader-vue
```

## Usage

In your vue component, import the vue skeleton loader

```vue
<script>
import SkeletonLoaderVue from 'skeleton-loader-vue'
export default {
  components: { SkeletonLoaderVue },
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
