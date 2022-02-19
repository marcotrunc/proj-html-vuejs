<template>
  <div class="container-fluid py-8 bs-nero">
    <div class="container mt-5">
      <div class="row">
        <div class="col-6">
          <figure>
            <img src="../assets/img/home_img-compressor.jpg" alt="img-gym" />
          </figure>
        </div>
        <div class="col-6">
          <h4 class="text-white mb-5">Sign Up For A Free Traning Session!</h4>
          <FormField label-text="Name..*" input-id="name" />
          <FormField label-text="Email" input-id="email" />
          <button class="w-100 py-3 mt-3">start now!</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import FormField from "./FormField.vue";

export default {
  name: "Form",
  components: { FormField },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
.container-fluid {
  background-color: $shark;
}

button {
  background-color: $bs-rose;
  border: none;
  text-transform: uppercase;
  color: white;
}
</style>