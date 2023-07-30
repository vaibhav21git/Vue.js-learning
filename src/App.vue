<template>
  <div>
    <h2 v-once>{{ name }}</h2>
    <button @click="name = 'manu'">Change name</button>
    <h2 v-pre>{{ name }}</h2>

    // used when you do not want to Compile html elements
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "vaibhav",
    };
  },

  methods: {},
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
