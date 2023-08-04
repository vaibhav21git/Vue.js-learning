<template>
  <div>
    <input
      type="text"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
  name: "InputF",
  props: {
    modelValue: String,
  },
};
</script>

<style lang="scss" scoped></style>
