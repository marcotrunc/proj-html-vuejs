<template>
  <section class="container-fluid bs-black-lg py-7">
    <div class="container py-7 h-100">
      <Title title-text="performance news" />
      <div class="row h-100 g-5 flex-column align-items-center">
        <div
          class="col-12 col-md-4"
          v-for="(card, index) in newsCards"
          :key="index"
        >
          <Cards
            :imgUrl="card.imgUrl"
            :title="card.title"
            :text="card.text"
            :bk-col="'bs-black'"
            :isColumn="true"
            :notSocial="true"
            :isFilter="true"
          />
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
import Cards from "./Cards.vue";
export default {
  name: "News",
  components: {
    Title,
    Btn,
    Cards,
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
    margin-top: 20px;
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, -100%);
  }
}

@media only screen and (max-width: 768px) {
  .container-fluid {
    height: 4200px;
  }
}
</style>