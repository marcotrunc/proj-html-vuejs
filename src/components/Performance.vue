<template>
  <section class="high-performance-facilities py-7">
    <div class="container">
      <Title title-text="High Performance facilities" />
      <Cards
        :list="imgCards"
        :not-Social="true"
        :not-text="true"
        :isScaled="true"
      />
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import Cards from "./Cards.vue";
export default {
  name: "Performance",
  components: {
    Title,
    Cards,
  },
  data() {
    return {
      imgCards: [
        { imgUrl: "home-image1.jpg", alt: "img" },
        { imgUrl: "home-image2.jpg", alt: "img" },
        { imgUrl: "home-image3.jpg", alt: "img" },
        { imgUrl: "home-image4.jpg", alt: "img" },
        { imgUrl: "home-image54.jpg", alt: "img" },
        { imgUrl: "home-image6.jpg", alt: "img" },
      ],
    };
  },
};
</script>

