<template>
  <div>
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }} {{ slotProps.lastName }}
      </template>
    </NameList>

    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.lastName }} {{ slotProps.firstName }}
      </template>
    </NameList>

    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }}
      </template>
    </NameList>
  </div>
</template>

<script>
// import CardV from "./components/CardV.vue";
import NameList from "./components/NameList.vue";

export default {
  name: "App",

  components: { NameList },

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
