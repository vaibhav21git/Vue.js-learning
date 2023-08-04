<template>
  <div>
    <h2>This is a Popup</h2>
    <button @click="$emit('close', 'vaibhav')">Close Popup</button>
  </div>
</template>

<script>
export default {
  name: "PopUp",
  emits: ["close"],
};
</script>

<style lang="scss" scoped></style>
