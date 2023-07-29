<template>
  <div>
    <div>
      <h2>{{ name }}</h2>
    </div>
    <div>
      <button v-on:click="changeName($event), increment(1, $event)">
        Change name
      </button>
    </div>
    <h2>{{ count }}</h2>
    <button @click="increment(5, $event)">Increment</button>
    <button v-on:click="decrement(2)">Decrement</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "vaibhav",
      count: 0,
    };
  },

  methods: {
    increment(num, event) {
      console.log(event);
      return (this.count += num);
    },

    changeName(event) {
      this.name = "manu";
      console.log("Event", event);
    },

    // to access the data() in method  you have to use this which represent an object

    decrement(num) {
      return (this.count -= num);
    },
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
