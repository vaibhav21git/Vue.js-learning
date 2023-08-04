<template>
  <div>
    <ComponentC />
    <h3>Appcomponent username {{ name }}</h3>
  </div>
</template>

<script>
import ComponentC from "./components/ComponentC.vue";

export default {
  name: "App",
  components: {
    ComponentC,
  },

  data() {
    return {
      name: "vaibhav",
    };
  },

  provide: {
    username: "vaibhav",
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>
