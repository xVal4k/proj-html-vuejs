<template>
  <div id="app">
    <header-pizza />
    <main-pizza />
    <footer-pizza />
  </div>
</template>

<script>
/* eslint-disable */

import HeaderPizza from './components/HeaderPizza.vue'
import MainPizza from './components/MainPizza.vue';
import FooterPizza from './components/FooterPizza.vue';

export default {
  name: 'App',
  components: {
    HeaderPizza,
    MainPizza,
    FooterPizza,
  },
};
</script>

<style lang="scss">
@import './assets/styles/style.scss'
</style>
