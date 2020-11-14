
<template>
  <div id="app">
    <div class="backgroundImg" id="home">
      <Navbar/>
      <Home id="home"/>
    </div>
      <router-view />
    <Menu id="menu"/>
    <Services id="services" />
    <About id="about" class="margin" />
    <Footer id="footer" />
  </div>
</template>

<script>
import Navbar from "./components/Nav"
import Home from "./components/Home";
import Menu from "./components/Menu";
import About from "./components/About";
import Services from "./components/Services";
import Footer from "./components/footer";

export default {
  name: "app",
  components: {
    Navbar,
    Home,
    Menu,
    About,
    Services,
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

@media only screen and (max-width: 500px) {
  .backgroundImg {
    height: 60vh;
  }
}

</style>