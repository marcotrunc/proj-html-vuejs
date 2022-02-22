<template>
  <div class="container-fluid bs-dark">
    <div
      id="home"
      class="container h-100-vh d-flex flex-column pt-2 position-relative"
    >
      <!-- Top Header -->
      <section
        id="top-header"
        class="row justify-content-between align-items-center bg-transparent"
      >
        <!-- Logo -->
        <div class="col-3 col-md-2">
          <div id="logo" class="text-light">
            <img
              src="../assets/img/gym_logo_1x.png"
              alt="logo"
              class="img-fluid"
            />
          </div>
        </div>
        <!-- Navbar -->
        <div class="col-9 col-md-10 d-flex justify-content-end">
          <nav class="text-light pt-4">
            <ul id="menu" class="d-none d-md-flex">
              <li v-for="(item, index) in navItems" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </nav>
          <!-- Hamburger Menù -->
          <div class="d-md-none p-5 position-relative" @click="isVisible">
            <div class="hamb-menu mb-1"></div>
            <div class="hamb-menu mb-1"></div>
            <div class="hamb-menu"></div>
          </div>
          <div id="menu-hamb" v-show="visibility">
            <ul class="d-flex flex-column">
              <li v-for="(item, index) in navItems" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
            <div class="cross px-2" @click="isVisible">
              <i class="fa-solid fa-xmark text-black fa-2x"></i>
            </div>
          </div>
        </div>
      </section>
      <!--Header Content-->
      <section id="banner" class="flex-grow-1">
        <div class="text-center py-7">
          <h1 class="text-uppercase fs-big text-white mb-5">No pain no gain</h1>
          <p class="text-white fs-4 mb-5">
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
  data() {
    return {
      visibility: false,
    };
  },
  methods: {
    isVisible() {
      if (this.visibility === false) return (this.visibility = true);
      return (this.visibility = false);
    },
  },
};
</script>

<style lang="scss" scoped>
#home {
  background-image: url("../assets/img/home-banner.jpg");
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  .hamb-menu {
    background-color: white;
    width: 30px;
    height: 3px;

    cursor: pointer;
  }
}
#banner {
  h1 {
    font-weight: 700;
  }
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
#menu-hamb {
  position: absolute;
  top: 15%;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 2;
  ul {
    background-color: #fff;
    list-style-type: none;
    text-align: center;
    padding-left: 0;
    li {
      padding: 20px;
      &:hover {
        color: #fff;
        background: lightgrey;
      }
      a {
        text-decoration: none;
        color: #000;
        text-transform: uppercase;
      }
    }
  }
  .cross {
    position: absolute;
    top: 0;
    right: 0;
    cursor: pointer;
  }
}
</style>