<template>
  <div>
    <GreetM name="Bruce" />
    <GreetM name="Clark" />
    <GreetM name="Diana" />
    <ArticleV title="Article Title" :likes="50" :isPublished="true" />
  </div>
</template>

<script>
import GreetM from "./components/GreetM.vue";
import ArticleV from "./components/ArticleV.vue";

export default {
  name: "App",
  components: {
    GreetM,
    ArticleV,
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
