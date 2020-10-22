<template>
  <div class="menu">
    <tabs>
      
      <tab name="Chef's Special" :selected="true">
        <div class="menuContent">
         
          
          <div class="card">
            <img src="../assets/Image1(1)chef'sSpecial.png" alt="">
            <div class="details">
              <p class="storyline" :Specials="Specials"> {{ Specials.phrase }} </p>
              <h3 class="name"> {{ Specials.name}} </h3>
              <p class="description"> 
                <pre>
                   {{Specials.description}}
                </pre>
               </p>
            </div>
          </div>
        </div>
      </tab>
      <tab name="Main course">
        <div class="menuContent">
          <h1>This is the main Menu</h1>
        </div>
      </tab>
      <tab name="Cake Deserts">
        <div class="menuContent">
          <h1>This are desserts</h1>
        </div>
      </tab>

    </tabs>
  </div>
</template>

<style scoped>
.menu {
  text-align: center;
  padding: 30px;
}
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

<script>
import tabs from "./tabs";
import tab from "./tab";

export default {
  name: "menu",
  components: {
    tabs,
    tab,
  },
  data() {
    return {
      Specials: [
        {
          id: 1,
          phrase: "Set the mood...",
          name: "Chocholate Cake",
          description:
            "Mini lemony pancakes with cheese, swis andblossoms garnish"
        },
        {
          id: 2,
          phrase: "Set the mood...",
          name: "Chocholate Cake",
          description:
            "Mini lemony pancakes with cheese, swis andblossoms garnish"
        },
      ],
    };
  },
};
</script>