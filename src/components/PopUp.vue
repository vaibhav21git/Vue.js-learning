<template>
  <div>
    <h2>This is a Popup</h2>
    <input type="text" v-model="name" />
    <button @click="$emit('close', name)">Close Popup</button>
  </div>
</template>

<script>
export default {
  name: "PopUp",
  // emits: ["close"],
  // for validation function mention the emit in the form of key-value pairs
  emits: {
    close: (name) => {
      if (!name) {
        return false;
      } else {
        return true;
      }
    },
  },
  data() {
    return {
      name: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>
