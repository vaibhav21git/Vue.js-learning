<template>
  <div>
    <h4>App component text</h4>
    <ChildStyles>ChildStyles component text</ChildStyles>
  </div>
</template>

<script>
import ChildStyles from "./components/ChildStyles.vue";

export default {
  name: "App",

  components: { ChildStyles },

  data() {
    return {};
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

<!-- 
here the orange color is restricted to its own not passed to the child 
if we try to use the scoped -->

<!-- scoped attribute ensures a component CSS will apply only to its own HTML elements -->

<!-- when using slots , the parent styles is applied and not the child 
component style even though the content is embedded inside the child
component -->
