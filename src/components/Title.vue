<template>
  <div class="text-white text-center mt-5">
    <div>
      <h2 class="d-inline-block text-uppercase">{{ titleText }}</h2>
      <span class="h3"> {{ specificText }}</span>
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
</style>