<template>
  <!-- Container -->
  <div class="container-fluid py-7">
    <div class="container py-7">
      <div class="row">
        <!-- v-for -->
        <div
          v-for="(card, index) in adCards"
          :key="index"
          class="col-3 text-white text-center"
        >
          <!-- Single Card -->
          <div>
            <div class="d-flex justify-content-center mb-3">
              <figure>
                <i class="fa-solid fa-3x text-rose" :class="card.icon"></i>
              </figure>
            </div>
            <h5>{{ card.title }}</h5>
            <img
              src="../assets/img/divider-x-red.png"
              alt="card.title"
              class="my-2"
            />
            <p class="text-grey">
              {{ card.paragraph }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Advantage",

  data() {
    return {
      adCards: [
        {
          icon: "fa-link-slash",
          title: "Stength & Conditioning",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, ornare es volutpa etra us. ",
        },
        {
          icon: "fa-bicycle",
          title: "Fitness & Cardio",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, ornare es volutpa etra us. ",
        },
        {
          icon: "fa-cloud",
          title: "Flexibility & Rest",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, ornare es volutpa etra us. ",
        },
        {
          icon: "fa-heart-pulse",
          title: "Health & Diet",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, ornare es volutpa etra us. ",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/_mixin.scss";
.container-fluid {
  background-image: url("../assets/img/gym_bkgd_bw-compressor.jpg");
  background-position: center;
  background-size: cover;
  figure {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    border: 2px solid $chestnut-rose;
    box-shadow: 0px 0px 0px 0px $chestnut-rose;
    @include centralizes-flex;

    &:hover {
      // @include scale(0.9);
      @include animation-options(shadow-incr, 2s, forwards);
    }
  }
}
@keyframes shadow-incr {
  0% {
    border: 2px solid $chestnut-rose;
    box-shadow: 0px 0px 0px 0px $chestnut-rose;
  }
  25% {
    border: 25px solid transparent;
    box-shadow: 0px 0px 2px 15px $chestnut-rose;
  }
  50% {
    border: 45px solid transparent;
    box-shadow: 0px 0px 2px 15px $chestnut-rose;
  }
  75% {
    border: 50px solid transparent;
    box-shadow: 0px 0px 2px 15px $chestnut-rose;
  }
  100% {
    border: 2px solid $chestnut-rose;
    box-shadow: 0px 0px 0px 0px $chestnut-rose;
  }
}
</style>