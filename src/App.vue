<template>
  <teleport to="#portal-root">
    <PortalV />
  </teleport>
</template>

<script>
import PortalV from "./components/PortalV.vue";
// teleporting allows to move elements from one place to another
// It is used to create component in a place and render it in the
// different place that is not under the root element which
// is under app

export default {
  name: "App",

  components: { PortalV },

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
