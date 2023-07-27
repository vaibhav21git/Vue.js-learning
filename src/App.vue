<template>
  <div>
    <h2 v-if="num === 0">The number is zero</h2>
    <h2 v-else-if="num < 0">The number is negative</h2>
    <h2 v-else-if="num > 0">The number is positive</h2>
    <h2 v-else>Not a number</h2>

    <template v-if="display === true">
      <h2>vaibhav</h2>
      <h2>vaibhav_utuber</h2>
      <h2>Vue</h2>
    </template>

    <h2 v-show="showElement">using v-show</h2>
    // if the condtion is false then the v-show will be toggled // to display :
    none and always presnt in DOM // but in case of v-if // it will not be
    present in the dom if the condition is false
    <h2 v-if="showElement">using v-if</h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      num: "hi",
      display: true,
      showElement: true,
    };
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
