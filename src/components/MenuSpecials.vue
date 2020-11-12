<template>
  <div class="menuContent">
    <div class="card" v-for="special of specials" :key="special.id">
      <img :src="require('@/assets/' + special.imgSrc)" alt="">
      <div class="details">
        <p class="storyline"> {{ special.phrase }} </p>
        <h3 class="name"> {{ special.name }} </h3>
        <p class="description"> 
          <pre>
              {{ special.description }}
          </pre>
          </p>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data: () => ({
    publicPath: process.env.BASE_URL,
    specials: [
      {
        id: 1,
        phrase: "Set the mood...",
        name: "Chocholate Cake",
        description:
          "Mini lemony pancakes with cheese, swis andblossoms garnish",
        imgSrc: "Image1(1)chef'sSpecial.png"
      },
      {
        id: 2,
        phrase: "Set the mood...",
        name: "Chocholate Cake",
        description:
          "Mini lemony pancakes with cheese, swis andblossoms garnish",
        imgSrc: "Image1(1)chef'sSpecial.png"
      },
    ]
  })
}
</script>

<style scoped>
.menuContent {
  text-align: left;
  background-color: #f1f6f7;
  margin: 13px 100px;
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
  border-radius: 20px;
  /* border: 1px solid black; */
  display: flex;
}
.details {
  padding: 100px 10px;
  text-align: right;
}
.storyline {
  font-family: "Tillana", cursive;
  font-weight: 300;
}
.name {
  font-size: 30px;
  color: #d36200;
  font-weight: 600;
  margin: 20px;
}
.description {
  font-weight: lighter;
}
pre {
  font-family: Work Sans;
}
</style>