<template>
  <div class="project wrapper" id="project">
    <h1> Project </h1>
    <div class="project-box">
        <ul v-for="(item, index) in contents" :key="index">
            <li class="project-box__item item-right" >
                <img :src="item.img" alt="">
                <article>
                    <h3 class="project-box__title"> Title: {{item.title}} <br> </h3> 
                    <div v-if="item.subtitles != '' "></div>
                        <ul class="project-box__subtitles" v-for="(_item, _index) in item.subtitles" :key="_index"> →　{{_item}} </ul>
                    <p class="project-box__detail"> {{ item.detail }} </p>
                </article>
            </li>
        </ul>
    </div>
  </div>
</template>

<script lang="ts">
export default {
    name: "Member",
    data: () => {
        return {
            contents: [
                {title: "SNSにおける情報拡散", subtitles: ["実空間とサイバー空間での拡散とその社会実装", "情報拡散シミュレーション"], img: "./sanolab/research/emotion.png", detail:"this is detail"},
                {title: "サイバー空間からの空気感の抽出", subtitles: ["新型コロナウィルス影響下での緊張感の変化", "高齢ドライバーに対する風当たりの可視化"], img: "./sanolab/research/spreadInfo.png", detail:"論文に記述される謝辞から学術界の人間関係を示す謝辞ネットワークを構築し、新たな視点から学術界と科学の発展を科学します"},
                {title: "謝辞から抽出した学術ネットワーク", subtitles: "", img: "./sanolab/research/acknowledgement.png", detail:"論文に記述される謝辞から学術界の人間関係を示す謝辞ネットワークを構築し、新たな視点から学術界と科学の発展を科学します"},
                {title: "人間活動におけるバースト性", subtitles: ["乳幼児と大人の違い"], img: "./sanolab/research/burst.png", detail:"this is detail"},
                {title: "保育現場のICT化", subtitles: ["ドアの開閉ログを用いた忙しさの定量化", "動線データの分析"], img: "./demo.jpg", detail:"this is detail"}
            ]
        }
    }
}

</script>

<style scoped>
#project {
    color: white;
    background-image: linear-gradient(rgb(245, 18, 18, 0.5), rgb(15, 15, 240,  0.5));
    background-repeat: repeat-x;
    height: 120vh;
}
.project {
  text-align: center;
  
}
.member-img {
    width: 100%;
    object-fit: cover;
}
h1{
    text-align: center;
    font-size: 3rem;
    padding-top: 20px;
}

ul li {
    list-style: none;
}

.project-box__item {
    border-top: 1px solid black;
    padding-top: 20px;
    margin: 20px auto;
}
.project-box__item img {
    width: 30%;
    margin-left: 60px;
}
.item-right {
    display: flex;
    justify-content:space-between;
}
article {
    margin-right: 60px;
}
</style>
