<template>
  <div class="social py-3" :class="{ 'd-none': notSocial }">
    <a
      href="#"
      v-for="(item, index) in socialList"
      :key="index"
      class="bs-black"
      :class="{ 'bs-pink': isPink }"
    >
      <i class="fa-brands text-white fa-lg" :class="item.name"></i
    ></a>
  </div>
</template>

<script>
export default {
  name: "SocialIcons",
  props: ["notSocial", "socialList", "isPink"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/_mixin.scss";
.social {
  display: flex;
  width: 50%;
  justify-content: space-between;

  a {
    padding: 5px;
    display: block;
    height: 45px;
    width: 45px;
    border: 1px solid $shark;
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    &:hover {
      background-color: $shark;
    }
  }
}
</style>