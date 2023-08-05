<template>
  <div>
    <h3 v-for="name in names" :key="name.firstName">
      <slot :firstName="name.firstName" :lastName="name.lastName"> </slot>
    </h3>
  </div>
</template>

<!-- // slot props -->
<script>
export default {
  name: "NameList",
  data() {
    return {
      names: [
        {
          firstName: "vaibhav",
          lastName: "Sachdeva",
        },
        {
          firstName: "ram ",
          lastName: "mishra",
        },
        {
          firstName: "shyam",
          lastName: "kumar",
        },
      ],
    };
  },
};
</script>

<style scoped></style>
