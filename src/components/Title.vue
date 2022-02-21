<template>
  <div class="text-white text-center mt-5">
    <div>
      <h2 class="d-inline-block text-uppercase">{{ titleText }}</h2>
      <span> {{ specificText }}</span>
    </div>
    <figure class="my-4">
      <img src="../assets/img/divider-xx-red.png" alt="divider" />
    </figure>
  </div>
</template>

<script>
export default {
  name: "Title",
  props: ["titleText", "specificText"],
};
</script>

<style lang="scss" scoped>
h2 {
  font-weight: 700;
  font-size: 2.3rem;
}
span {
  font-size: 2.2rem;
  font-weight: 700;
}
</style>