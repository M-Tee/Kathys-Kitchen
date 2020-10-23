<template>
  <div class="menu">
    <h2 class="heading">Menu</h2>
    <div class="tabs menuNav">
      <ul>
        <li
          v-for="tab in tabs"
          :key="tab"
          :class="{ 'is-active': tab.isActive }"
        >
          <a :href="tab.href" @click="selectTab(tab)">{{ tab.name }}</a>
        </li>
      </ul>
    </div>

    <div class="tabs-details">
      <tab name="Chef's Special" :selected="true">
        <div  class="menuContent">
          <scard :key="content.id" v-for="content in Specials" :content="content" class="card"></scard>
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
    </div>
  </div>
</template>

<style scoped>
.heading {
  margin-bottom: 20px;
  font-family: "Tillana", cursive;
  font-size: 2.5vw;
  color: #d36200;
}
.menuNav {
  margin-bottom: 30px;
}

.menuNav a {
  text-decoration: none;
  color: rgba(0, 0, 0, 0.7);
  margin: 0 30px;
  letter-spacing: 0.2em;
  font-size: 1.4vw;
}

.menuNav a:hover,
.is-active {
  color: #d36200;
  border-bottom: 3px solid #d36200;
  padding-bottom: 8px;
}

ul li {
  display: inline-block;
}
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
  display: flex;
}
.card{
  margin: 0;
  display: flex;
  flex-direction: column;
}
.menuContent :nth-child(2){
    flex-direction: column-reverse;
}


</style>

<script>
import tab from "./tab";
import scard from "./sCard";

export default {
  name: "tabs",
  components: {
    tab,
    scard,
  },
  data() {
    return {
      tabs: [
        {
          id: 1,
          name: "Chef's Special",
          selected: true,
        },
        {
          id: 2,
          name: "Main Course",
        },
        {
          id: 3,
          name: "Cake Desserts",
        },
      ],
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

  created() {
    this.tabs = this.$children;
  },
  methods: {
    selectTab(selectedTab) {
      this.tabs.forEach((tab) => {
        tab.isActive = tab.name == selectedTab.name;
      });
    },
  },
};
</script>