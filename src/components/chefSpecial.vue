<template>
  <div class="con-tainer margin menuContent">
    <scard
      :key="content.id"
      v-for="content in Specials"
      :content="content"
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
.menuContent {
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
}
.menuContent :nth-child(2) {
  flex-direction: column-reverse;
}

@media only screen and (max-width: 600px) {
  .menuContent {
    box-shadow: unset;
  }
  .con-tainer {
    flex-direction: row;
  }
}
</style>