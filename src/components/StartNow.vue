<template>
  <div class="container-fluid py-8 bs-nero">
    <div class="container mt-5">
      <div class="row">
        <!-- Block left -->
        <div class="col-6">
          <figure>
            <img src="../assets/img/home_img-compressor.jpg" alt="img-gym" />
          </figure>
        </div>
        <!-- Form Block -->
        <div class="col-6">
          <h4 class="text-white mb-5">Sign Up For A Free Traning Session!</h4>
          <Form :fields="inputs" btn-text="start now!" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Form from "./Form.vue";
export default {
  name: "StartNow",
  components: {
    Form,
  },
  data() {
    return {
      inputs: [
        { type: "text", id: "name", title: "Name..." },
        { type: "text", id: "email", title: "Email" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
.container-fluid {
  background-color: $shark;
  h4 {
    font-weight: 600;
  }
}
</style>