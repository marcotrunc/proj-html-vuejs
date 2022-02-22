<template>
  <div class="container-fluid py-8 bs-nero">
    <div class="container mt-5">
      <div class="row">
        <!-- Block left -->
        <div class="col-12 col-md-6">
          <figure>
            <img
              src="../assets/img/home_img-compressor.jpg"
              alt="img-gym"
              class="img-fluid"
            />
          </figure>
        </div>
        <!-- Form Block -->
        <div class="col-12 col-md-6 mt-3 mt-md-0">
          <h4 class="text-white mb-5">Sign Up For A Free Traning Session!</h4>
          <!-- Field -->
          <div>
            <label for="userName" class="text-grey">Name...</label>
            <input
              type="text"
              id="userName"
              class="d-block mb-3 w-100 text-white"
              v-model="userName"
            />
            <label for="email" class="text-grey">Email</label>
            <input
              type="email"
              id="email"
              class="d-block mb-3 w-100 text-white"
              v-model="email"
              pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$"
            />
          </div>
          <!-- Button -->
          <button class="w-100 py-3 mt-3 fs-5" @click="showMessage">
            Start now
          </button>
          <div class="message mt-4 px-4" v-show="isSend">
            <h5 class="text-grey p-3">
              Ciao {{ userName }}, ti abbiamo inviato una mail di conferma
              all'indirizzo: {{ email }}.
            </h5>
            <div class="cancel" @click="cancelMessage">
              <i class="fa-solid fa-xmark text-grey"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StartNow",
  components: {},
  data() {
    return {
      userName: "",
      email: "",
      isSend: false,
    };
  },
  methods: {
    showMessage() {
      if (this.userName && this.email) {
        this.isSend = true;
      }
    },
    cancelMessage() {
      this.userName = "";
      this.email = "";
      this.isSend = false;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/_mixin.scss";
.container-fluid {
  background-color: $shark;
  h4 {
    font-weight: 600;
  }
  img {
    transition: transform 0.5s;
    &:hover {
      transform: scale(1.06);
    }
  }
  input {
    background-color: $shark-black;
    line-height: 2.2rem;
    border: 1px solid $dove-grey;
    &:hover {
      border: none;
    }
  }
  button {
    background-color: $bs-rose;
    border: none;
    text-transform: uppercase;
    color: white;
  }
  .message {
    position: relative;
    border: 1px solid $dove-grey;
    .cancel {
      position: absolute;
      top: 0;
      right: 0;
      @include centralizes-flex;
      border-bottom: 1px solid $dove-grey;
      border-left: 1px solid $dove-grey;
      padding: 5px;
      cursor: pointer;
    }
  }
}
</style>