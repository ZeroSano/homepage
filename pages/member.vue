<template>
  <div class="member wrapper" id="member">
    <h1> Member </h1>
    <div class="member-introduction">
        <!-- 学年ごと -->
        <ul v-for="(values, grade) in members" :key="grade">
            <h2 class="member-grade" v-if="grade==='Leader'"> {{grade}}</h2>
            <h2 class="member-grade" v-else> Grade: {{ grade }} </h2>
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
                Leader: [
                    {name: 'Yukie Sano', img: "./face.jpg", comment: "Sano sensei"}
                    ],
                m2: [
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"},
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"},
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"},
                    {name: 'm2tarou', img: "./face.jpg", comment: "hi, i'm m2 trou"}, {name: 'm2 no m2', img: "./face.jpg", comment: "hi, i'm m2 no m2"}
                ],
                m1: [{name: 'm1 yo', img: "./face.jpg", comment: "hi, i'mm1 yoyo"}, {name: 'm1 m1 ', img: "./face.jpg", comment: "hi, m1 m1"}],
                b4: [{name: 'b4b4b4b', img: "./face.jpg", comment: "b4b4"}, {name: 'bbb4', img: "./face.jpg", comment: "hi, bbbb444"}]
            }
        }
    }
}

</script>

<style scoped>
#member {
    background-image: linear-gradient(rgb(238, 183, 183), rgb(180, 180, 228));
    /* background-blend-mode: luminosity; */
    background-repeat: repeat-x;
    height: 200vh;
}
.home {
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
ul > li {
    list-style: none;
}


.member-grade{
    border-bottom: 1px solid black;
}
.member-grade__box{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    
    gap: 1px;
}
.member-item {
    background-color: rgb(126, 169, 204);
    padding: 5px;
    max-width: 240px;
    margin-bottom:20px;
}

</style>
