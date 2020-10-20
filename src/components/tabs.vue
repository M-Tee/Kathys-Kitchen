<template>
  <div>
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
      <slot></slot>
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
.is-active{
  color: #d36200;
  border-bottom: 3px solid #d36200;
  padding-bottom: 8px;
}

ul li {
  display: inline-block;
}
</style>

<script>
export default {
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