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
        <chefSpecial/>
      </tab>

      <tab name="Main course">
        <div class="menuContent">
          <mainCourse> </mainCourse>
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

<script>
import tab from "./tab";
import chefSpecial from "./chefSpecial";
import mainCourse from "./mainCourse";


export default {
  name: "tabs",
  components: {
    tab,
    chefSpecial,
    mainCourse,
  },
  data() {
    return {
      tabs: [],
     
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


</style>