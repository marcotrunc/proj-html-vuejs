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
  border: 2px solid $dove-grey;
  padding: 10px 25px;
  color: $dove-grey;
  text-transform: uppercase;
  transition: border 1s, color 1s;
  &:hover {
    border: 2px solid #fff;
    color: #fff;
  }
}
</style>