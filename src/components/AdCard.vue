<template>
  <div>
    <div class="d-flex justify-content-center mb-3">
      <figure>
        <i class="fa-solid fa-3x text-rose" :class="icon"></i>
      </figure>
    </div>
    <h5>{{ title }}</h5>
    <img src="../assets/img/divider-x-red.png" alt="cancel" class="my-2" />
    <p class="text-grey">
      {{ paragraph }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["icon", "title", "paragraph"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
figure {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  border: 2px solid $chestnut-rose;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>