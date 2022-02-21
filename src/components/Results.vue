<template>
  <div class="container-fluid py-7">
    <section id="real-world-results" class="py-7">
      <div class="container">
        <Title title-text="Real World Results" />
        <div class="row g-5">
          <div v-for="(card, index) in ResCards" :key="index" class="col-6">
            <ResCard
              :imgUrl="card.imgUrl"
              :text="card.text"
              :signature="card.signature"
            />
          </div>
        </div>
      </div>
    </section>

    <Performance />
  </div>
</template>

<script>
import Title from "./Title.vue";
import ResCard from "./ResCard.vue";
import Performance from "./Performance.vue";
export default {
  name: "Results",
  components: {
    Title,
    ResCard,
    Performance,
  },
  data() {
    return {
      ResCards: [
        {
          imgUrl: "review_1-compressor.jpg",
          text: "The trainers at Avada Gym have helped me reach my fitness goals beyond anything I could of hoped for. I love it!",
          signature: "Tara Smith",
        },
        {
          imgUrl: "review_3-compressor-2.jpg",
          text: "The atmosphere at Avada Gym is amazing, the people are even better. All in all, it is a great place to work out.",
          signature: "Simon Chel",
        },
        {
          imgUrl: "review_2-compressor.jpg",
          text: "The facilities at Avada Gym stood out to me the most. They are well maintained and have high quality equipment.",
          signature: "Jen Wirth",
        },
        {
          imgUrl: "review_4-compressor-2.jpg",
          text: "No bad things to say about Avada Gym, they are top notch at every corner and truly take care of their customers.",
          signature: "Jeff Glum",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
.container-fluid {
  background-color: $shark-black;
}
</style>