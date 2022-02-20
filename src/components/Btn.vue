<template>
  <button class="fs-5">{{ textBtn }}</button>
</template>

<script>
export default {
  name: "Btn",
  props: ["textBtn"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
button {
  background-color: transparent;
  border: 1px solid $dove-grey;
  padding: 10px 25px;
  color: $dove-grey;
  text-transform: uppercase;
}
</style>