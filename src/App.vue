<template>
  <InputF v-model="name" />
</template>

<script>
// import PopUp from "./components/PopUp.vue";
import InputF from "./components/InputF.vue";

export default {
  name: "App",

  components: {
    // PopUp,
    InputF,
  },

  data() {
    return {
      name: "",
    };
  },

  methods: {},

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
