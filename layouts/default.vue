<template>
  <div class="default">
    <Navigation />

    <Nuxt />
  </div>
</template>

<script>
import Navigation from '../components/navigation'
export default {
  Navigation
}

</script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

.wrapper {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 4px;
}
.default {
   background-image: url("/nature.jpg");
    background-size:cover;                 /* 画像のサイズを指定    */
}
</style>
