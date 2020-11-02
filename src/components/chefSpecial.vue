<template>
  <div class="container menuContent">
    <scard
      :key="content.id"
      v-for="content in Specials"
      :content="content"
      class="card"
    ></scard>
  </div>
</template>

<script>
import scard from "./sCard";

export default {
  name: "chefspecial",
  components: {
    scard,
  },
  data() {
    return {
      Specials: [
        {
          id: 1,
          image: require("../assets/miniPancakes.png"),
          phrase: "Set the mood...",
          name: "Mini Pancakes",
          description:
            "Mini lemony pancakes with cheese, swis andblossoms garnish",
        },
        {
          id: 2,
          image: require("../assets/PastaImage.png"),
          phrase: "Dig In...",
          name: "Italian Pasta",
          description:
            "Mini lemony pancakes with cheese, swis andblossoms garnish",
        },
        {
          id: 3,
          image: require("../assets/cakeImage.png"),
          phrase: "Wrap Up...",
          name: "Chocholate Cake",
          description:
            "Mini lemony pancakes with cheese, swis andblossoms garnish",
        },
      ],
    };
  },
};
</script>

<style scoped>

.card {
  margin: 0;
  display: flex;
  flex-direction: column;
}
.menuContent{
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
}
.menuContent :nth-child(2) {
  flex-direction: column-reverse;
  margin-top: -1px;
}

@media only screen and (max-width: 600px) {
  .menuContent :nth-child(2) { 
    flex-direction: column;
  }
}
</style>