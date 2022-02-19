<template>
  <section class="py-7">
    <div
      class="
        container-fluid
        d-flex
        justify-content-center
        align-items-center
        h-90-vh
        mb-5
      "
    >
      <div class="text-white text-center quote">
        <p class="fs-2">
          "I fear not the man who has practiced 10,000 kick once, but I fear the
          man who has practiced one kick 10,000 times"
        </p>
        <h5 class="text-uppercase">Bruce Lee - quote of the day</h5>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Banner",
};
</script>

<style lang="scss" scoped>
.container-fluid {
  background-image: url("../assets/img/home-testimonial-bg.jpg");
  background-position: center;
  background-size: cover;

  .quote {
    width: 50%;
  }
}
</style>