<template>
  <div>
    <h2 class="heading">Menu</h2>
    <div class="tabs menuNav">
      <ul>
        <li
          v-for="menuSection in menuSections"
          :key="menuSection.route"
          :class="{ 'is-active': $route.name === menuSection.route }"
        >
          <router-link :to="{name: menuSection.route}">{{ menuSection.name }}</router-link>
        </li>
      </ul>
    </div>

    <div class="tabs-details">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    menuSections: {
      type: Array,
      required: true,
      validator: value => {
        /*
          Just making sure that this prop is an array of objects with string name and string route parameters
        */
        return !value.some(item => {
          return typeof item !== 'object' ||
                  typeof item.name !== 'string' ||
                  typeof item.route !== 'string'
        })
      }
    }
  },
  data() {
    return { tabs: [] };
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
.is-active{
  color: #d36200;
  border-bottom: 3px solid #d36200;
  padding-bottom: 8px;
}

ul li {
  display: inline-block;
}
</style>