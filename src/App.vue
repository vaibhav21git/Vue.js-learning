<template>
  <div>
    <button @click="showPopup = true">Show Popup</button>
    <PopUp v-show="showPopup" @close="closepopup" />
  </div>
</template>

<script>
import PopUp from "./components/PopUp.vue";

export default {
  name: "App",
  components: {
    PopUp,
  },

  data() {
    return {
      name: "vaibhav",
      showPopup: false,
    };
  },

  methods: {
    closepopup(name) {
      this.showPopup = false;
      console.log("name", name);
    },
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
