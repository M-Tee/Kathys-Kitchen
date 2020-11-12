<template>
  <div class="menu">
    <tabs :menu-sections="menuSections" />
    <router-view />

  </div>
</template>

<script>
import tabs from "./tabs";
// import tab from "./tab";

export default {
  name: "menu",
  components: {
    tabs,
    // tab,
  },
  data() {
    return {
      menuSections: [
        {
          name: 'Chef Specials',
          route: 'menu.specials'
        },
        {
          name: 'Main Courses',
          route: 'menu.mainCourse'
        },
        {
          name: 'Cake Desserts',
          route: 'menu.cakeDesserts'
        }
      ],
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