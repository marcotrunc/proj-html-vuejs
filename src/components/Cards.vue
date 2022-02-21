<template>
  <div class="row h-100 g-5" :class="{ 'flex-column': isColumn }">
    <div class="col-4" v-for="(card, index) in list" :key="index">
      <div :class="bkCol">
        <!-- Img -->
        <img
          :src="require(`../assets/img/${card.imgUrl}`)"
          :alt="card.title"
          class="img-fluid"
        />
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
  props: ["list", "bkCol", "notSocial", "isColumn", "notText", "socialList"],
  components: {
    SocialIcons,
  },
};
</script>

