<template>
  <div class="container-fluid bs-dark">
    <div id="home" class="container h-100-vh d-flex flex-column pt-2">
      <!-- Top Header -->
      <section
        id="top-header"
        class="row justify-content-between align-items-center bg-transparent"
      >
        <!-- Logo -->
        <div class="col-2">
          <div id="logo" class="pt-4 text-light">
            <img
              src="../assets/img/gym_logo_1x.png"
              alt="logo"
              class="img-fluid"
            />
          </div>
        </div>
        <!-- Navbar -->
        <div class="col-10 d-flex justify-content-end">
          <nav class="text-light pt-4">
            <ul id="menu">
              <li v-for="(item, index) in navItems" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </nav>
        </div>
      </section>

      <!--Header Content-->
      <section id="banner" class="flex-grow-1">
        <div class="text-center pt-4">
          <h1 class="text-uppercase fs-big text-white mb-5">No pain no gain</h1>
          <p class="text-white fs-4">
            Motivation is what gets you stared. Habit is what keeps you going
          </p>
          <Btn text-btn="Join us Today" />
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import Btn from "./Btn.vue";
export default {
  name: "Header",
  props: ["navItems"],
  components: {
    Btn,
  },
};
</script>

<style lang="scss" scoped>
#home {
  background-image: url("../assets/img/home-banner.jpg");
  background-position: center;
  background-size: cover;
}

#menu {
  display: flex;

  li {
    list-style-type: none;
    margin: 0 10px;
    cursor: pointer;
    a {
      text-decoration: none;
      text-transform: uppercase;
      color: #ffffff;
    }
  }
}
</style>