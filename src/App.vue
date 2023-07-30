<template>
  <div>
    <h2>fullname - {{ firstName }} {{ lastName }}</h2>
    <h2>Computed fullname -{{ fullName }}</h2>
    <button @click="items.push({ id: 4, title: 'Keyboard', price: 50 })">
      Add item
    </button>
    <h2>Computed Total - {{ total }}</h2>
    <h2>Method Total - {{ getTotal }}</h2>
    <input type="text" v-model="country" />

    <template v-for="item in items" :key="item.id">
      <h2 v-if="item.price > 100">{{ item.title }} {{ item.price }}</h2>
    </template>

    <h2 v-for="item in expensiveItems" :key="item.id">
      {{ item.title }} {{ item.price }}
    </h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "vaibhav",
      lastName: "sachdeva",
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
    };
  },

  //in  methods , properties  will always be recalculated on typing also , as the page
  // is re-rendered
  methods: {
    getTotal() {
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },

  // like methods you added the computed property
  //computed is basically an object
  // computed object contains a key which is a computed property
  //what we have done is composed a new data property from a existing data property
  // why should we use computed properties over data properties
  //1)properties need to be rendered to multiple places
  // computed properties are automatically calculated if their dependency changes
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 100);
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
