<template>
  <div>
    <div>
      <pre>
     {{ JSON.stringify(formValues, null, 2) }}
  </pre
      >
    </div>
    <form>
      <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model="formValues.name" />
      </div>
      <div>
        <label for="profile">Profile Summary</label>
        <textarea id="profile" v-model="formValues.profileSummary" />
      </div>
      <div>
        <label for="country">Country</label>
        <select id="country" v-model="formValues.country">
          <option value="">select a country</option>
          <option value="India">India</option>
          <option value="Russia">Russia</option>
          <option value="China">China</option>
        </select>
      </div>

      //control click is required
      <div>
        <label for="jobLocation">jobLocation</label>
        <select id="jobLocation" multiple v-model="formValues.jobLocation">
          <option value="India">India</option>
          <option value="Russia">Russia</option>
          <option value="China">China</option>
        </select>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
      },
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
