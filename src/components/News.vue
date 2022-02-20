<template>
  <section class="container-fluid bs-black-lg py-7">
    <div class="container py-7 h-100">
      <Title title-text="performance news" />
      <div class="row flex-column h-100 gx-5 gy-5">
        <div class="col-4" v-for="(card, index) in newsCards" :key="index">
          <div class="bs-dark">
            <figure>
              <img
                :src="require(`../assets/img/${card.imgUrl}`)"
                :alt="card.title"
                class="img-fluid"
              />
            </figure>
            <div class="description p-4 fs-6">
              <h4 class="text-white">
                {{ card.title }}
              </h4>
              <p class="text-grey lh-lg">
                {{ card.text }}
              </p>
            </div>
          </div>
        </div>
      </div>
      <section class="button">
        <Btn textBtn="Read all articles" />
      </section>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import Btn from "./Btn.vue";
export default {
  name: "Vue",
  components: {
    Title,
    Btn,
  },
  data() {
    return {
      newsCards: [
        {
          imgUrl: "blog1.jpg",
          title: "Train with free weights or your body weight?",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]",
        },
        {
          imgUrl: "blog4.jpg",
          title: "To be number one, train like you're number two",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]",
        },
        {
          imgUrl: "blog6.jpg",
          title: "Nutritional advice that will keep you training",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]",
        },
        {
          imgUrl: "trainer3.jpg",
          title: "Top 5 mistakes every gym member makes",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]",
        },
        {
          imgUrl: "trainer4.jpg",
          title: "Simple principles for your next workout",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]",
        },
        {
          imgUrl: "trainer1.jpg",
          title: "The myths of shedding body fat explored",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container-fluid {
  height: 1800px;
  position: relative;
  .button {
    position: absolute;
    top: 100%;
    left: 50%;
    transform: translate(-50%, -200%);
  }
}
</style>