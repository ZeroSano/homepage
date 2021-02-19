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
                        <p>Name: {{ value.name }}</p>
                        <p>Comment: {{ value.comment }}</p>
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
            members: {
                Director: [
                    {name: 'Yukie Sano', img: "./face.jpg", comment: "Sano sensei"}
                    ],
                M2: [
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"},
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"},
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"},
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"}
                ],
                M1: [{name: 'm1 yo', img: "./face.jpg", comment: "hi, i'mm1 yoyo"}, {name: 'm1 m1 ', img: "./face.jpg", comment: "hi, m1 m1"}],
                B4: [{name: 'b4b4b4b', img: "./face.jpg", comment: "b4b4"}, {name: 'bbb4', img: "./face.jpg", comment: "hi, bbbb444"}]
            }
        }
    }
}
</script>

<style scoped>
#member {
    background-color: rgba(158, 173, 162, 0.7);
    /* background-blend-mode: luminosity; */
    /* background-repeat: repeat-y; */
    height: 200vh;
}
.home {
  text-align: center;
  
}
.member-img {
    /* width: 100%; */
    border-radius: 50%;
    width: 250px;
    height: 250px;
    
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

</style>
