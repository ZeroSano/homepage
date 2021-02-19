<template>
  <div class="home wrapper" id="home">
    <h1> Sano Lab </h1> 
    <div class="contents">
      佐野研究室では社会を対象に社会物理学の視点から研究しています。
      <br>
      <img class="intro" src="sanolab/intro.png" alt="">
    </div>
  </div>
</template>

<script lang="ts">
// import Vue from 'vue'

// export default Vue.extend({})
</script>

<style scoped>
#home {
  background-image: url("/HP_Photo/IMG_0447.jpg"), linear-gradient(rgb(159, 163, 155), rgb(123, 124, 119));
  object-fit: cover;
  background-blend-mode: hard-light;
  background-repeat: repeat-y;
  height: 100vh;
  color: white;
}
.home {
  text-align: center;
}

h1{
  padding-top: 100px;
}
.intro {
  width: 90%;
}
</style>
