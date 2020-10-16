<template>
  <div id="app">
    <div class="backgroundImg">
      <div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="">Menu</router-link>
        <router-link to="">Order</router-link>
        <router-link to="">About</router-link>
        <!-- <router-link to="/about">About</router-link> -->
      </div>
      <router-view />
    </div>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Tillana:wght@800&family=Work+Sans:wght@500&display=swap");

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
}

.backgroundImg {
  background-image: url("./assets/edited-brooke-lark-08boynh_r_e.jpg");
  background-repeat: no-repeat;
    background-position: center top;

  background-size: cover;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 90vh;
}

#nav {
  text-align: right;
  margin-top: 70px;
  margin-right: 70px;
  font-style: normal;
  font-weight: 300;
  font-size: 1.4vw;
  line-height: 28px;
  letter-spacing: 0.2em;
}

#nav a {
  font-weight: bold;
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
@media only screen and (max-width: 768px) {
  .backgroundImg {
    background-position: center;
  }
}
@media only screen and (max-width: 600px) {
  #nav{
    margin-right: 25px;

  }
}

@media only screen and (max-width: 500px) {
  .backgroundImg{
    height: 60vh;
  }
  #nav{
    display: none;
  }
}


</style>