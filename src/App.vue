<template>
  <div id="app">
    <StartPage />
    <BodyPage />
  </div>
</template>

<script>
import './assets/normalize.css';
import StartPage from './components/StartPage.vue';
import BodyPage from './components/BodyPage.vue';

export default {
    name: "App",
    components: { StartPage, BodyPage }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  font-family: 'SF Pro Text';
}
@font-face {
  font-family: 'SF Pro Display';
  src: url('./assets/fonts/Display/SFProDisplay-Heavy.woff2') format('woff2');
  font-weight: 800;
}
@font-face {
  font-family: 'SF Pro Display Bold';
  src: url('./assets/fonts/Display/SF-Pro-Display-Bold.21a7ca44.woff2') format('woff2');
  font-weight: 600;
}
@font-face {
  font-family: 'SF Pro Text';
  src: url('./assets/fonts/Text/SF-Pro-Text-Regular.woff2') format('woff2');
}
</style>
