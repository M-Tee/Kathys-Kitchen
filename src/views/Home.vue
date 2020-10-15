<template>
  <div class="home" >
    <h1 class="brandName">Kathy's Kitchen</h1>
    <p class="catchphrase">A little slice of Heaven</p>
    <Button class="menuBtn">Today's Menu</Button>
  </div>
</template>

<style scoped>
.home{
text-align: right;
margin-right: 70px;
}
.brandName{
font-family: 'Tillana', cursive;
font-size: 80px;
color: #D36200;
padding-top: 150px;
}
.catchphrase{
margin: 20px;
  font-size: 36px;
  font-weight: 500;
  line-height: 42px;
}
.menuBtn{
  margin: 70px;
  font-size: 24px;
}

</style>

<script>
// @ is an alias to /src
      // import HelloWorld from '@/20px/HelloWorld.vue'
// import backgroundImg from '../assets/brooke-lark-08bOYnH_r_E-unsplash.jpg';
import Button from '../components/button';

export default {
  name: 'Home',
  components: {
    Button,
  }
}
</script>
