<template>
  <div>
    <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>

    <!-- <TabA v-if="activeTab === 'TabA'" />
    <TabB v-if="activeTab === 'TabB'" />
    <TabC v-if="activeTab === 'TabC'" /> -->

    <!-- v-bind is same as : -->

    <!-- which component to render is decided by :is in component -->

    <keep-alive>
      <component :is="activeTab" />
    </keep-alive>
  </div>
</template>

<!-- 
if the user is filling the form in differernt tab then the data should be 
preserved in each tab for the better user experience -->
<!-- for this we use key alive element -->
<!-- here vue is keeping dynamic component alive even when the component is not
active -->

<script>
import TabA from "./components/TabA.vue";
import TabB from "./components/TabB.vue";
import TabC from "./components/TabC.vue";

export default {
  name: "App",

  components: { TabA, TabB, TabC },

  data() {
    return {
      activeTab: "TabA",
    };
  },

  methods: {},
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h4 {
  color: orange;
}
</style>
