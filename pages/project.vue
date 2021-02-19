<template>
  <div class="project wrapper" id="project">
    <h1> Project </h1>
    <div class="project-box">
        <ul v-for="(item, index) in contents" :key="index">
            <li class="project-box__item item-right" >
                <img :src="item.img" alt="">
                <article>
                    <h3> Title: {{item.title}} <br> </h3> 
                    <p v-if="item.subtitle!=''"> Subtitle:  {{item.subtitle}} </p>
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
                {title: "SNSにおける情報拡散", subtitle: "実空間とサイバー空間での拡散とその社会実装", img: "./demo.jpg"},
                {title: "SNSにおける情報拡散", subtitle: "情報拡散シミュレーション", img: "./demo.jpg"},
                {title: "サイバー空間からの空気感の抽出", subtitle: "新型コロナウィルス影響下での緊張感の変化", img: "./demo.jpg"},
                {title: "サイバー空間からの空気感の抽出", subtitle: "高齢ドライバーに対する風当たりの可視化", img: "./demo.jpg"},
                {title: "謝辞から抽出した学術ネットワーク", subtitle: "", img: "./demo.jpg"},
                {title: "人間活動におけるバースト性", subtitle: "乳幼児と大人の違い", img: "./demo.jpg"},
                {title: "保育現場のICT化", subtitle: "ドアの開閉ログを用いた忙しさの定量化", img: "./demo.jpg"},
                {title: "保育現場のICT化", subtitle: "動線データの分析", img: "./demo.jpg"},
                {title: "スポーツデータの分析", subtitle: "少年サッカーにおけるボールタッチ回数分析", img: "./demo.jpg"}               
            ]
        }
    }
}

</script>

<style scoped>
#project {
    background-image: linear-gradient(rgb(245, 18, 18), rgb(15, 15, 240));
    background-repeat: repeat-x;
    height: 100vh;
}
.project {
  text-align: center;
  
}
.member-img {
    width: 100%;
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
    border-bottom: 1px solid black;
    padding-bottom: 20px;
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
