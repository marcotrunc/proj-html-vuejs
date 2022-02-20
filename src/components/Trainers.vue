<template>
  <section class="container-fluid position-relative bs-black py-6">
    <div class="container">
      <Title title-text="Meet our Trainers" />

      <div class="row gx-5">
        <div v-for="(card, index) in trainers" :key="index" class="col-4">
          <div class="bs-black-lg">
            <figure>
              <img
                :src="require(`../assets/img/${card.imgUrl}`)"
                :alt="card.name"
                class="img-fluid"
              />
            </figure>
            <div class="text p-5">
              <h5 class="text-white">{{ card.name }}</h5>
              <h5 class="text-white mb-4">{{ card.role }}</h5>
              <p class="text-grey fs-6 lh-lg">{{ card.descr }}</p>
              <div class="social">
                <a href="#"
                  ><i class="fa-brands text-white fa-facebook-f fa-lg"></i
                ></a>
                <a href="#"
                  ><i class="fa-brands text-white fa-twitter fa-lg"></i
                ></a>
                <a href="#"
                  ><i class="fa-brands text-white fa-instagram fa-lg"></i
                ></a>
              </div>
            </div>
          </div>
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
export default {
  name: "Trainers",
  components: {
    Title,
    Btn,
  },
  data() {
    return {
      trainers: [
        {
          imgUrl: "trainer1.jpg",
          name: "Ann Baker",
          role: "Personal Trainer",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat.",
        },
        {
          imgUrl: "trainer3.jpg",
          name: "Anne Warren",
          role: "Personal Trainer",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat.",
        },
        {
          imgUrl: "trainer4.jpg",
          name: "Peter Rice",
          role: "Personal Trainer",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";

.social {
  display: flex;
  width: 50%;
  justify-content: space-between;
  a {
    padding: 5px;
    display: block;
    height: 45px;
    width: 45px;
    border: 1px solid $shark;
    border-radius: 8px;
    background-color: $shark;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
  }

  .arrow-down {
    background-color: $shark;
  }
}
</style>