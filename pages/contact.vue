<template>
  <div class="contact wrapper" id="contact">
    <h1> contact </h1> 

    <div class="access">
        <h2>Direction</h2>
        1 Chome-1ｰ1 Tennodai, Tsukuba, Ibaraki 305-8577
        <h2>Email</h2>
        <a href = "mailto: sano@sk.tsukuba.ac.jp">sano@sk.tsukuba.ac.jp</a>
    </div>

  </div>
</template>

<script lang="ts">
// import Vue from 'vue'

// export default Vue.extend({})
</script>

<style scoped>
#contact {
  background-image: url("/HP_Photo/IMG_0447.jpg"), linear-gradient(rgb(159, 163, 155), rgb(123, 124, 119));
  object-fit: cover;
  background-blend-mode: hard-light;
  background-repeat: repeat-y;
  height: 100vh;
  color: white;
}
.contact {
  text-align: center;
}

h1{
  padding-top: 100px;
  font-size: 3rem;
}
a {
  /* text-decoration: none; */
  color: white;
}
</style>
