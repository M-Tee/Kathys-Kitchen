<template>
   <div class="home">
    <h1 class="brandName">Kathy's Kitchen</h1>
    <p class="catchphrase">A little slice of Heaven</p>
    <Button class="menuBtn">Today's Menu </Button>
</div>
</template>

<style scoped>
  .home {
    text-align: right;
    margin-right: 70px;
  }
  .brandName {
    font-family: "Tillana", cursive;
    font-size: 5.1vw;
    color: #d36200;
    margin-top: 150px;
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

<script>
// @ is an alias to /src
// import HelloWorld from '@/20px/HelloWorld.vue'
// import backgroundImg from '../assets/brooke-lark-08bOYnH_r_E-unsplash.jpg';
import Button from "../components/button";

export default {
  name: "Home",
  components: {
    Button,
  },
  
};
</script>
