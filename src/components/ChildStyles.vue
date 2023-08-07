<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "ChildStyles",
};
</script>

<style>
h4 {
  color: forestgreen;
}
</style>

<!-- 
parent style is evaluated at the last so if you provide separated child style 
then also the parent style is applied their -->
<!-- if you write scoped then this can be ignored -->
<!-- EXCEPTION IN CASE OF ROOT ELEMENT  which is without div 
inside just inside of the template -->
