<template>
  <div class="member wrapper" id="member">
    <h1> Member </h1>
    <div class="member-introduction">
        <!-- 学年ごと -->
        <ul v-for="(values, grade) in members" :key="grade">
            <h2 class="member-grade" v-if="grade==='Director'"> {{grade}}</h2>
            <h2 class="member-grade" v-else> {{ grade }} </h2>
            <!-- 各学年内での記述 -->
            <div class="member-grade__box">
                <ul v-for="(value, key) in values" :key="key">
                    <li class="member-item">
                        <img class="member-img" :src="value.img" alt="">
                        <p>{{ value.name_en }} </p>
                    </li>
                </ul>
            </div>
        </ul>
    </div>
  </div>
</template>

<script lang="ts">
export default {
    name: "Member",
    data: () => {
        return {
            baseURL: process.env.baseUrl,
            members: {
                PI: [
                    {name_en: 'Yukie Sano', img: "sanolab/profile/ST__028r.JPG"}
                    ],
                D1: [
                    {name_en: 'Makoto Takeuchi', img: "sanolab/profile/D1_takeuchi.jpg"}
                    ],
                M2: [
                    {name_en: 'Ren Chohira', img: "sanolab/profile/face.jpg"},
                    {name_en: 'Tsubasa Asano', img: "sanolab/profile/face.jpg"}
                ],
                M1: [
                    {name_en: 'Ryou Azuma', img: "sanolab/profile/M1_azuma.JPG"},
                    {name_en: 'Naoki Igarashi ', img: "sanolab/profile/M1_Igarashi.jpg"},
                    {name_en: 'Li Zijing', img: "sanolab/profile/face.jpg"}, 
                    {name_en: 'Zhang Ruojing', img: "sanolab/profile/face.jpg"}
                ],
                B4: [
                    {name_en: 'Mitsuya Asaka', img: "sanolab/profile/face.jpg"},
                    {name_en: 'Keigo Kusumegi', img: "sanolab/profile/B4_kusumegi.JPG"},
                    {name_en: 'Chika Namiki', img: "sanolab/profile/B4_namiki.JPG"}
                    ],
                B3: [
                    {name_en: 'Otomo', img: "sanolab/profile/B3_otomo.jpg"}
                    ],
                "Research Student": [
                    {name_en: 'Chung Ming Hui', img: "sanolab/profile/R1_Min.JPG"}
                    ]
            }
        }
    }
}
</script>

<style scoped>
#member {
    background: linear-gradient(rgb(245, 18, 18, 0.5), rgb(15, 15, 240,  0.5));
    height: 100%;
}
.home {
  text-align: center;
  
}
.member-img {
    /* width: 100%; */
    border-radius: 10%;
    object-fit: cover; 
    width: 250px;
    height: 300px;
    
}
h1{
    text-align: center;
    font-size: 3rem;
    padding-top: 20px;
}
ul > li {
    list-style: none;
}


.member-grade{
    border-bottom: 1px solid black;
    padding-right: 20px;
}
.member-grade__box{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1px;
    padding-right: 20px;
}
.member-item {
    background-color:rgb(rgb(156, 114, 114), rgb(155, 175, 155), rgb(124, 124, 161), 0.);
    padding: 5px;
    max-width: 200px;
    margin-bottom:20px;
    margin:20px 0;
}
.member-item p {
    font-size: 1.3rem;
    text-align: center;
}

@media (min-width: 800px) {

}
</style>
