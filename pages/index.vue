<template>
  <div class="home wrapper" id="home" :style="{background: `url('${ baseURL }HP_Photo/IMG_7151.jpg')`, 'background-color': 'rgb(100, 236, 130, .2)', 'background-blend-mode': '  background-blend-mode:luminosity'}">
    <h1> 複雑系研究室　Sano Lab </h1> 
    <div class="contents">
      佐野研究室ではインターネット上の人間の行動・心理から実社会での行動まで、幅広い社会全体を対象に <br> 数理モデルを活用してその構造を理解していきます。
    </div>

    <hooper class="hopper-contents" :autoPlay="true" :playSpeed="6000">
      <slide class="hopper-contents__item" v-for="(item, index) in slides" :key="index">
        <h3> Research topic {{ index + 1 }} </h3> 
        <img class="intro" :src="item.img" :alt="item.alt"> <br>
        <!-- <p>  {{ item.description }}</p> -->
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
  },
  data: () => {
        return {
          baseURL: process.env.baseUrl,
            slides: [
              {img: "sanolab/research/intro.png", alt:"acknowledgement", description: ""},
              {img: "sanolab/research/emotion.png", alt:"acknowledgement", description: "this is emotion"},
              {img: "sanolab/research/spreadInfo.png", alt:"acknowledgement", description: "this is spreadInfo"},
              {img: "sanolab/research/acknowledgement.png", alt:"acknowledgement", description: "this is acknow"},
              {img: "sanolab/research/burst.png", alt:"acknowledgement", description: "this is burst"},
            ]
      }
  }
}
</script>

<style scoped>
#home {
  /* background-image: url("/HP_Photo/IMG_0447.jpg"), linear-gradient(rgb(159, 163, 155), rgb(123, 124, 119)); */
  object-fit: cover;
  background-blend-mode:luminosity;
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
.contents{
  width: 80%;
  margin: 20px auto;
  font-size: 1.25rem;
}
.intro {
  width: 90%;
}

.hopper-contents{
  height: 850px;
  width: 90%;
  margin: 20px auto;
}

.hooper-slide {
    /* background-color: #d9dddc; */
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    border: 2px solid #fff;
    font-size: 30px;
    border-radius: 10px;
  }

.hopper-contents__item {
  display: flex;
  flex-direction: column;
  padding: 0;
}
.hopper-contents__item h3 {
  margin: 10px auto;
}
.hopper-contents__item p {
  margin: 0;
}

@media (max-width: 800px) {
.hopper-contents{
  height: 550px;
  width: 90%;
  margin: 20px auto;
}
}

</style>
