<template>
  <div id="app">
    <header-page></header-page>
    <main-page></main-page>
  </div>
</template>

<script>
import HeaderPage from './components/HeaderPage.vue';
import MainPage from './components/MainPage.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
  },
};
</script>

<style lang="scss">
$main_color_1: #2E3A46;
$main_color_2: #1E2D3B;
@import "~bootstrap/scss/bootstrap";
img{
  max-width: 100%;
}
html{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
