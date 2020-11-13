<template>
  <div id="nav">
        <router-link to="#" v-scroll-to="'#home'" >Home</router-link>
        <router-link to="#" v-scroll-to="'#menu'" >Menu</router-link>
        <router-link to="#" v-scroll-to="'#services'" >Service</router-link>
        <router-link to="#" v-scroll-to="'#about'" >About</router-link>
      </div>
</template>
<script>
export default {
  name: "navbar"
}
</script>

<style scoped>
#nav {
  text-align: right;
  padding-top: 70px;
  margin-right: 70px;
  font-weight: 400;
  font-size: 1em;
  line-height: 28px;
  letter-spacing: 0.2em;
}

#nav a {
  color: #2c3e50;
  text-decoration: none;
  margin-left: 70px;
}
#nav a:hover {
  color: #d36200;
}

#nav a.router-link-exact-active {
  /* color: #D36200; */
}

/* 
#nav a.router-link-exact-active {
  color: #D36200;
} */


</style>