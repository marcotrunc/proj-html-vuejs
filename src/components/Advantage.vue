<template>
  <div class="container-fluid py-7">
    <div class="container mt-5">
      <div class="row">
        <div
          v-for="(card, index) in adCards"
          :key="index"
          class="col-3 text-white text-center"
        >
          <AdCard
            :icon="card.icon"
            :title="card.title"
            :paragraph="card.paragraph"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AdCard from "./AdCard.vue";
export default {
  name: "Advantage",
  components: {
    AdCard,
  },
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
.container-fluid {
  background-image: url("../assets/img/gym_bkgd_bw-compressor.jpg");
  background-position: center;
  background-size: cover;
}
</style>