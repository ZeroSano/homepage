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
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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

@media (max-width: 1200) {
  .wrapper {
  max-width: 80%;
  margin: 0 auto;
  padding: 0 4px;
}
  
}
</style>
