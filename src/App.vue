<template>
  <div>
    <header>
      <h1>Our Projects</h1>
      <TabNav :tabs="['Digital Products', 'Brand Studio']" :selected="selectedTab" @selected="setSelectedTab" />
    </header>

    <main>
      <Tab :isSelected="selectedTab === 'Digital Products'">
        <DynamicContent :content="digitalProducts" />
      </Tab>
      <Tab :isSelected="selectedTab === 'Brand Studio'">
        <DynamicContent :content="brandStudio" />
      </Tab>
    </main>
  </div>
</template>

<script>
import TabNav from './components/TabNav.vue';
import Tab from './components/Tab.vue';
import DynamicContent from './components/DynamicContent.vue';
import { projectsData } from './projectsData';

export default {
  components: { TabNav, Tab, DynamicContent },
  data() {
    return {
      selectedTab: 'Digital Products',
      digitalProducts: {},
      brandStudio: {}
    };
  },
  created() {
    this.digitalProducts = projectsData.digitalProducts,
    this.brandStudio = projectsData.brandStudio
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    }
  }
};
</script>

<style scoped>
header {
  margin-bottom: 20px;
  text-align: center;
}

main {
  padding: 20px;
}
</style>
