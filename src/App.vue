<template>
  <div>
    <div>
      <pre>
     {{ JSON.stringify(formValues, null, 2) }}
  </pre
      >
    </div>
    <form @submit.prevent="submitForm">
      <div>
        // use of lazy modifier and trim
        <label for="name">Name</label>
        <input type="text" id="name" v-model.trim.lazy="formValues.name" />
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

      <div>
        <input
          type="checkbox"
          id="remoteWork"
          v-model="formValues.remoteWork"
          true-value="yes"
          false-value="no"
        />
        <label for="remoteWork">Open to remote work?</label>
      </div>

      <div>
        <label>skill set</label>
        <input
          type="checkbox"
          id="html"
          value="html"
          v-model="formValues.skillset"
        />
        <label for="html">HTML</label>
        <input
          type="checkbox"
          id="css"
          value="css"
          v-model="formValues.skillset"
        />
        <label for="css">css</label>
        <input
          type="checkbox"
          id="js"
          value="js"
          v-model="formValues.skillset"
        />
        <label for="js">js</label>
      </div>

      <div>
        <label for="age">Age</label>
        <input
          @keyup.enter="submitForm"
          type="number"
          id="age"
          v-model.number="formValues.age"
        />
      </div>
      <!-- <div><button>Submit</button></div> -->
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
        remoteWork: "no",
        skillset: [],
        age: null,
      },
    };
  },

  methods: {
    submitForm() {
      console.log("Form values", this.formValues);
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
