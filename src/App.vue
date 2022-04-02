<template>
  <div id="app">
    <header-pizza />
    <main-pizza />
  </div>
</template>

<script>
/* eslint-disable */

import HeaderPizza from './components/HeaderPizza.vue'
import MainPizza from './components/MainPizza.vue';
export default {
  name: 'App',
  components: {
    HeaderPizza,
    MainPizza,
  },
};
</script>

<style lang="scss">
@import './assets/styles/style.scss'
</style>
