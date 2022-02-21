<template>
  <div class="bs-black-lg">
    <Header :nav-items="navItems" />
    <main>
      <Description />
      <StartNow />
      <Advantage />
      <Results />
      <Banner />
      <Trainers />
      <News />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Description from "./components/Description.vue";
import StartNow from "./components/StartNow.vue";
import Advantage from "./components/Advantage.vue";
import Results from "./components/Results.vue";
import Banner from "./components/Banner.vue";
import Trainers from "./components/Trainers.vue";
import News from "./components/News.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Description,
    StartNow,
    Advantage,
    Results,
    Banner,
    Trainers,
    News,
    Footer,
  },
  data() {
    return {
      navItems: [
        "Home",
        "About us",
        "Facilities",
        "Membership",
        "Testimonials",
        "Blog",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
