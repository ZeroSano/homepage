<template>
  <div class="contact wrapper" id="contact" :style="{ background:  `url('${baseURL}HP_Photo/IMG_7179.jpg')`, 'object-fit': 'cover'}">
    <h1> contact </h1> 

    <div class="access">
        <h2>Email</h2>
        <a href = "mailto: sano@sk.tsukuba.ac.jp">sano@sk.tsukuba.ac.jp</a>
        <h2>Direction</h2>
        1 Chome-1ｰ1 Tennodai, Tsukuba, Ibaraki 305-8577 <br>
        <p> <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d805.8292991070226!2d140.0990387881777!3d36.110129298749904!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60220bff0b159a83%3A0xac90e7d61d49d16b!2sInstitutes%20of%20Engineering%20Sciences%20F%2C%201-ch%C5%8Dme%20Tenn%C5%8Ddai%2C%20Tsukuba%2C%20Ibaraki%20305-0006!5e0!3m2!1sen!2sjp!4v1614843153207!5m2!1sen!2sjp" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe> </p>
        
    </div>

  </div>
</template>

<script lang="ts">
export default {
    name: "Member",
    data: () => {
        return {
          baseURL: process.env.baseUrl
        }
    }
}
</script>

<style scoped>
#contact {
  background-blend-mode: hard-light;
  background-repeat: repeat-y;
  height: 100vh;
  color: white;

  display:flex;
  flex-direction: column;

}
.contact {
  text-align: center;
}
h1{
  padding-top: 100px;
  font-size: 3rem;
}
h2 {
  border-bottom: 1px solid white;
  width: 60%;
  margin: 10px auto;
  padding: 20px;
}
.map {
  width: 80%;
}
a {
  /* text-decoration: none; */
  color: white;
}
</style>
