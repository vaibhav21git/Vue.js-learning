<template>
  <div>
    <CardV>Card Content</CardV>
    <CardV><h2>Card content</h2></CardV>
    <CardV>
      <img src="https://picsum.photos/200" />
    </CardV>
    <CardV></CardV>
  </div>
</template>

<script>
import CardV from "./components/CardV.vue";

export default {
  name: "App",

  components: { CardV },

  data() {
    return {};
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
