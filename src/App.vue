<template>
  <div>
    <h2 v-for="(name, index) in names" v-bind:key="name">
      {{ index }} {{ name }}
    </h2>
    <h2 v-for="(names, index) in fullNames" :key="index">
      {{ index }} {{ names.first }} {{ names.last }}
    </h2>
    <h2 v-for="names in fullNames" :key="names">
      {{ names.first }} {{ names.last }}
    </h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["vaibhav", "madhu", "rajarshi"],
      fullNames: [
        {
          first: "vaibhav",
          last: "sachdeva",
        },
        {
          first: "rajarshi",
          last: "chakraborty",
        },
        {
          first: "premkumar",
          last: "srivasana",
        },
      ],
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
