<template>
  <div>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{ actor.name }}</h2>
      <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
    </div>
    <h2 v-for="(value, key, index) in myInfo" :key="value">
      {{ index }} {{ key }} {{ value }}
    </h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["vaibhav", "madhu", "rajarshi"],
      actors: [
        {
          name: "vaibhav sachdeva",
          movies: ["oldscool", "jaiho"],
        },
        {
          name: "rajarshi chakraborty",
          movies: ["hanuman", "panchayat"],
        },
        {
          name: "premkumar srivasana",
          movies: ["malamaal weekly", "taxiwala"],
        },
      ],
      myInfo: {
        name: "vaibhav",
        channel: "vaibhav_utuber",
        course: "vue 3",
      },
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
