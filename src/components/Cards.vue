<template>
  <div class="row h-100 g-5" :class="{ 'flex-column': isColumn }">
    <div class="col-4" v-for="(card, index) in list" :key="index">
      <div :class="bkCol">
        <!-- Img -->
        <div class="position-relative img-contain">
          <img
            :src="require(`../assets/img/${card.imgUrl}`)"
            :alt="card.title"
            class="img-fluid"
            :class="{ scale: isScaled }"
          />
          <div class="filter" v-show="isFilter">
            <div class="icon-container">
              <i class="fa-solid fa-link text-white me-3"></i>
              <i class="fa-solid fa-magnifying-glass text-white"></i>
            </div>
          </div>
        </div>

        <!-- Text -->
        <div class="description p-4 fs-6" :class="{ 'd-none': notText }">
          <h4 class="text-white">
            {{ card.title }}
          </h4>
          <h4 class="text-white mb-4">{{ card.role }}</h4>
          <p class="text-grey fs-6 lh-lg">
            {{ card.text }}
          </p>
          <SocialIcons :not-social="notSocial" :social-list="socialList" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SocialIcons from "./SocialIcons.vue";
export default {
  name: "Cards",
  props: [
    "list",
    "bkCol",
    "notSocial",
    "isColumn",
    "notText",
    "socialList",
    "isScaled",
    "isFilter",
  ],
  components: {
    SocialIcons,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/_mixin.scss";

// Effect scale
.scale {
  @include transition(transform, 0.5s);
  &:hover {
    @include scale(1.06);
  }
}

// Effect Increasing-Width
.fa-solid {
  display: none;
}
.img-contain:hover .filter {
  @include pos-start;
  @include width-start;
  @include animation-options(increasing-width, 1s, forwards);
  background-color: $chestnut-rose;
  opacity: 0.75;
  display: block;
  .icon-container {
    @include centralizes;
  }
  .fa-solid {
    display: inline;
    cursor: pointer;
  }
}

@keyframes increasing-width {
  from {
    width: 0%;
  }
  to {
    width: 100%;
  }
}
</style>

