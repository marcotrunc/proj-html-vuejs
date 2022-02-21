<template>
  <div>
    <!-- Field -->
    <div v-for="(field, index) in fields" :key="index">
      <label for="field.id" class="text-grey">{{ field.title }}</label>
      <input
        type="field.type"
        id="field.id"
        class="d-block mb-3 w-100 text-white"
      />
    </div>
    <!-- Button -->
    <button class="w-100 py-3 mt-3 fs-5">{{ btnText }}</button>
  </div>
</template>

<script>
export default {
  name: "Form",
  props: ["fields", "btnText"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
input {
  background-color: $shark-black;
  line-height: 2.2rem;
  border: 1px solid $dove-grey;
}
button {
  background-color: $bs-rose;
  border: none;
  text-transform: uppercase;
  color: white;
}
</style>