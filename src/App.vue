
<template>
  <div id="app">
    <div class="backgroundImg" id="home">
      <div id="nav">
        <router-link to="/home">Home</router-link>
        <router-link to="/menu">Menu</router-link>
        <router-link to="/services">Service</router-link>
        <router-link to="/about">About</router-link>
      </div>
      <Home> </Home>
    </div>
      <router-view />
    <!-- <Menu id="menu"/>
    <Services id="services" />
    <About id="about" class="margin" /> -->
    <Footer id="footer" />
  </div>
</template>

<script>
import Home from "./components/Home";
// import Menu from "./components/Menu";
// import About from "./components/About";
// import Services from "./components/Services";
import Footer from "./components/footer";

export default {
  name: "app",
  components: {
    Home,
    // Menu,
    // About,
    // Services,
    Footer,
  },
};
</script>

<style>

* {
  padding: 0;
  margin: 0;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #f1f6f7;
  color: rgba(0, 0, 0, 0.7);
}

.backgroundImg {
  background-image: url("./assets/edited-brooke-lark-08boynh_r_e.jpg");
  background-repeat: no-repeat;
  background-position: center top;
  background-size: cover;
  margin-top: 0px;
  /* position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 100vh; */
}

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


#services {
  background: rgba(225, 236, 242, 0.59);
  margin: 0;
}

#menu,
#about,
#services {
  padding-top: 30px;
  padding-bottom: 90px;
}
/* Media Queries */
@media only screen and (max-width: 768px) {
  .backgroundImg {
    background-position: center;
  }
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

@media only screen and (max-width: 500px) {
  .backgroundImg {
    height: 60vh;
  }
  #nav {
    display: none;
  }
}
</style>