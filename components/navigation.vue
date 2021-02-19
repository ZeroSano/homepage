<template>
<header class="page-header wrapper">
  <!-- <h1> <nuxt-link to='/'> <img src="/logo.jpg" alt="logo"> </nuxt-link> </h1> -->
  <h1> <nuxt-link to="/"> Sano Lab </nuxt-link> </h1>


  <nav>
    <ul class="nav">
      <li class="nav-items" v-for="(item, index) in navItems" :key="index">
        <ul> <nuxt-link :to="item.path"> {{ item.title }} </nuxt-link> </ul>

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
  justify-content:space-between;
  background-color: rgb(129, 135, 153);
}
.nav {
display: flex;
margin: 10px;
}
.nav li {
  list-style: none;
  justify-content: center;
}
.nav li ul {
  margin-top: 20px;
  font-size: 1.2rem;
}
.nav li ul a:hover {
  color: red;
}
</style>
