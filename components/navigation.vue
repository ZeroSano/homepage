<template>
<header class="page-header wrapper" :style="{background: `url('${ baseURL }sanolab/network.png') left 210% top`}">
  <!-- <h1> <nuxt-link to='/'> <img src="/logo.jpg" alt="logo"> </nuxt-link> </h1> -->
  <h1> <nuxt-link to="/">Sano Lab</nuxt-link> </h1>

  <nav>
    <ul class="nav">
      <li class="nav-items" v-for="(item, index) in navItems" :key="index">
        <nuxt-link :to="item.path"> {{ item.title }} </nuxt-link>
      </li>
    </ul>
  </nav>

</header>
</template>

<script lang="ts">                                     
  export default {
      name: "NavigationBar",
      data: () => {
          return {
            baseURL: process.env.baseUrl,
              navItems: [
                  {path: '/',  title: 'Home'},
                  {path: '/member', title: 'Member'},
                  {path: '/project', title: 'Project'},
                  {path: '/contact', title: 'contact'}                    
              ]
          }
      }
  }
</script>

<style scoped>
.page-header {
  display: flex;
  flex-direction: column;
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
h1 {
  text-decoration: none;
  margin-bottom: 0;
  text-align: center;
}
a{
  text-decoration: none;
  color: rgb(40, 63, 44);
}
.nav {
  display: flex;
  justify-content: center;
  margin: 20px;
}
.nav li {
  list-style: none;
  margin: 5px 20px;
}
.nav li a {
  font-size: 1.3rem;
}
.nav li a:hover {
  color: rgb(227, 228, 230);
}
</style>
