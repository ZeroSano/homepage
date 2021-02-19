<template>
  <div class="home wrapper" id="home">
    <h1> Sano Lab </h1> 
    <div class="contents">
      佐野研究室では社会を対象に社会物理学の視点から研究しています。
    </div>


    <hooper class="hopper-contents" :autoPlay="true" :playSpeed="4000">
      <slide>
        slide 1
        <img class="intro" src="sanolab/intro.png" alt="">
      </slide>
      <slide>
        slide 2
        <img src="sanolab/emotion.png" alt="">
      </slide>
      <slide>
        slide 3
        <img class="intro" src="sanolab/spreadInfo.png" alt="">
      </slide>
      <slide>
        slide 4
        <img class="intro" src="sanolab/acknowledgement.png" alt="">
      </slide>
      <slide>
        slide 5
        <img class="intro" src="sanolab/burst.png" alt="">
      </slide>
      <slide>
        slide 6
        <img class="intro" src="demo.jpg" alt="">
      </slide>
      <hooper-pagination slot="hooper-addons"></hooper-pagination>
  </hooper>

  </div>
</template>

<script>
import { Hooper, 
         Slide,
         Pagination as HooperPagination, // ページネーションが必要なときにimport
         Navigation as HooperNavigation  // 左右のナビゲーションが必要なときにimport
        } from 'hooper'
import 'hooper/dist/hooper.css' // hooperのcssを適用
export default {
  components: {
    Hooper,
    Slide,
    HooperPagination,
    HooperNavigation
  }
}
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

.hopper-contents{
  height: 800px;
}

.hooper-slide {
    background-color: #62caaa;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    border: 2px solid #fff;
    font-size: 30px;
    border-radius: 10px;
  }
</style>
