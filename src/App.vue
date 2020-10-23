
<template>
  <div id="app">
    <div class="backgroundImg">
      <div id="nav">
        <router-link to="/menu">Menu</router-link>
        <router-link to="/order">Order</router-link>
        <router-link to="/about">About</router-link>
        <!-- <router-link to="/about">About</router-link> -->
      </div>
      <div class="home">
        <h1 class="brandName">Kathy's Kitchen</h1>
        <p class="catchphrase">A little slice of Heaven</p>
        <Button class="menuBtn">Today's Menu</Button>
      </div>
    </div>
    <router-view />
  </div>
</template>

<script>
import Button from "./components/button.vue";
export default {
  components: { Button },
  name: "app",
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Tillana:wght@600;800&family=Work+Sans:wght@400;500;600&display=swap");

* {
  padding: 0;
  margin: 0;
}

#app {
  font-family: "Work Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: rgba(0, 0, 0, 0.7);
  background: #f1f6f7;
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
  font-size: 1.4vw;
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

@media only screen and (max-width: 500px) {
  .backgroundImg {
    height: 60vh;
  }
  #nav {
    display: none;
  }
}

.home {
    text-align: right;
    margin-right: 70px;
  }
  .brandName {
    font-family: "Tillana", cursive;
    font-size: 5.1vw;
    color: #d36200;
    padding-top: 150px;
  }
  .catchphrase {
    margin: 20px 0;
    font-size: 2.3vw;
    font-weight: 500;
    line-height: 42px;
  }
  .menuBtn {
    margin: 30px 0 100px;
    font-size: 1.8vw;
  }

  @media screen and (max-width: 768px) {
    .brandName {
    font-size: 30px;
    }
    .catchphrase{
      font-size: 14px;
    }
    .menuBtn{
      font-size: 11px;
    }
  }
  @media only screen and (max-width: 600px) {
    .home {
    margin-right: 25px;
    }
  }
</style>