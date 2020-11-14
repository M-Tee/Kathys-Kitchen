<template>
  <div id="nav">
    <!-- <router-link to="#" v-scroll-to="'#home'" >Home</router-link>
        <router-link to="#" v-scroll-to="'#menu'" >Menu</router-link>
        <router-link to="#" v-scroll-to="'#services'" >Service</router-link>
        <router-link to="#" v-scroll-to="'#about'" >About</router-link> -->
    <div>
      <b-navbar toggleable="md" type="light">
        <b-navbar-brand href="#"></b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"> </b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="#" v-scroll-to="'#home'">Home</b-nav-item>
            <b-nav-item href="#" v-scroll-to="'#menu'">Menu</b-nav-item>
            <b-nav-item href="#" v-scroll-to="'#service'">Service</b-nav-item>
            <b-nav-item href="#" v-scroll-to="'#about'">About</b-nav-item>
          </b-navbar-nav>
        </b-collapse>

      </b-navbar>
    </div>
  </div>
</template>
<script>
export default {
  name: "navbar",
};
</script>

<style scoped>
#nav {
  text-align: right;
  padding-top: 3em;
  margin-right: 70px;
  font-weight: 400;
  font-size: 1em;
  line-height: 28px;
  letter-spacing: 0.2em;
}

#nav a {
  color: #2c3e50;
  text-decoration: none;
  margin-left: 50px;
}
#nav a:hover {
  color: #d36200;
}

#nav a.router-link-exact-active {
  /* color: #D36200; */
}

.navbar,
a.nav-link {
  padding-right: unset;
}
.navbar-toggler-icon {
  color: #d36200;
}

@media only screen and (max-width: 600px) {
  #nav {
    margin-right: 25px;
  }
}

@media only screen and (max-width: 768px) {
  #nav {
    font-size: 0.8rem;
  }
}
</style>