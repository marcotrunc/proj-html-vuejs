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
button {
  background-color: transparent;
  border: 1px solid #fff;
  padding: 10px 25px;
  color: #fff;
  text-transform: uppercase;
}
</style>