<template>
  <div>
    <label for="inputId" class="text-grey">{{ labelText }}</label>
    <input type="text" id="inputId" class="d-block mb-3 w-100 text-white" />
  </div>
</template>

<script>
export default {
  name: "FormField",
  props: ["labelText", "inputId"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
input {
  background-color: $shark-black;
  line-height: 2.2rem;
  border: 1px solid $dove-grey;
}
</style>