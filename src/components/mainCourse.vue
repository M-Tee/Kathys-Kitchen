<template>
  <div class="container">
    <card v-for="meal in meals" :key="meal.id" :meal="meal"> </card>
  </div>
</template>

<script>
import card from "./card";

export default {
  name: "maincourse",
  components: { card },
  data () {
    return {
      meals: [
        {
          id: 1,
          image: "friedChicken.png",
          name: "Fried chicken",
          description: "Fried chiken served with white rice and curry"
        },
        {
          id: 2,
          image: "chikenBiriyani.png",
          name: "Chicken Biriyani",
          description: "Chicken stew served with white rice"
        },
        {
          id: 3,
          image: "beefRibs.png",
          name: "Beef Ribs",
          description: "Beef ribs served with white rice and gravy"
        },
        {
          id: 4,
          image: "burgerNfries.png",
          name: "HamBurger and Fries",
          description: "Hamburger served with fries and hot sauce."
        },
        {
          id: 5,
          image: "pastaNmeatballs.png",
          name: "Pasta with Meatballs",
          description: "Sphaggeti with meat balls and tomato sauce"
        },
        {
          id: 6,
          image: "pastaShrimp.png",
          name: "Pasta with Shrimps",
          description: "Italian seasoned pasta with shrimps"
        }
      ]
    }
  }
  
}
</script>

<style scoped>
.container{
  display: flex;
  flex-wrap: wrap;
  margin: 13px 100px;
justify-content: center;
  
}
</style>
