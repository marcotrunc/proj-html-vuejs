<template>
  <section class="container-fluid position-relative bs-black py-7">
    <div class="container">
      <Title title-text="Meet our Trainers" />
      <div class="row h-100 g-5">
        <div
          class="offset-2 col-8 offset-lg-0 col-lg-4"
          v-for="(card, index) in trainers"
          :key="index"
        >
          <Cards
            :imgUrl="card.imgUrl"
            :title="card.title"
            :role="card.role"
            :text="card.text"
            :bk-col="'bs-black-lg'"
            :not-social="false"
            :isColumn="false"
            :socialList="socialList"
            :isScaled="true"
          />
        </div>
      </div>
      <div class="d-flex justify-content-center mt-5 py-5">
        <Btn text-btn="View all trainers" />
      </div>
      <div class="arrow-down"></div>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import Btn from "./Btn.vue";
import Cards from "./Cards.vue";
export default {
  name: "Trainers",
  components: {
    Title,
    Btn,
    Cards,
  },
  data() {
    return {
      trainers: [
        {
          imgUrl: "trainer1.jpg",
          title: "Ann Baker",
          role: "Personal Trainer",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat.",
        },
        {
          imgUrl: "trainer3.jpg",
          title: "Anne Warren",
          role: "Personal Trainer",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat.",
        },
        {
          imgUrl: "trainer4.jpg",
          title: "Peter Rice",
          role: "Personal Trainer",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat.",
        },
      ],
      socialList: [
        { name: "fa-facebook-f" },
        { name: "fa-twitter" },
        { name: "fa-instagram" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";

.arrow-down {
  background-color: $shark;
}
</style>