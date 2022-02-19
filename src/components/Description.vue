<template>
  <div class="container-fluid position-relative py-7">
    <section class="container">
      <div class="row flex-column align-items-center">
        <div class="col-4">
          <Title title-text="World Class" specificText="Fitness" />
        </div>
        <div class="col-10">
          <p class="text-grey text-center">
            At Avada Gym,everything we do from top to bottom is of the highest
            quality to ensure we're equipped to help you reach your goals of a
            healthy and fit lifestyle.
          </p>
        </div>
      </div>
    </section>
    <div class="arrow-down"></div>
  </div>
</template>

<script>
import Title from "./Title.vue";
export default {
  name: "Description",
  components: {
    Title,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
.container-fluid {
  background-color: $shark-black;
}

.arrow-down {
  position: absolute;
  left: 50%;
  top: 100%;
  transform: translate(-50%, 0%);
}
</style>