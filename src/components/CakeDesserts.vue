<template>
  <div class="con-tainer">
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
          image: "chocolateChip.png",
          name: "Chocolate Chip Cake",
          description: "Chocholate cake with Strawberry Icing"
        },
        {
          id: 2,
          image: "VanillaCakes.png",
          name: "Vanilla Cup cakes",
          description: "Vanilla cupcakes with nuts and chocolate"
        },
        {
          id: 3,
          image: "apricotPie.png",
          name: "Apricot Pie",
          description: "Apricot pie with nuts and honey"
        },
        {
          id: 4,
          image: "chocolateOreo.png",
          name: "Chocolate Oreo Cake",
          description: "Cholocate Oreo cake with vanilla icing and Oreo"
        },
        {
          id: 5,
          image: "lemonCake.png",
          name: "Lemon Cup Cake",
          description: "Lemmon cup cake with vanilla icing."
        },
        {
          id: 6,
          image: "fruitCake.png",
          name: "Fruit Cake",
          description: "Fruit Cup Cake with nuts topping "
        }
      ]
    }
  }
  
}
</script>

<style scoped>
.con-tainer{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
