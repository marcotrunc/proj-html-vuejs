<template>
  <div>
    <!-- Top Footer -->
    <section id="top-footer" class="py-7 container-fluid">
      <div class="container">
        <div class="row text-white align-items-center">
          <div class="col-12 col-md-10">
            <div>
              <h3>Achieve Your Fitness Goals</h3>
              <span class="fs-5">
                Flexible membership packages to suit alla levels of athelete and
                achive your fitness goals
              </span>
            </div>
          </div>
          <div class="col-12 col-md-2 mt-4 mt-md-0">
            <Btn textBtn="Join us" class="w-100" />
          </div>
        </div>
      </div>
    </section>
    <!-- Main Footer -->
    <section id="main-footer">
      <div class="container py-7">
        <div class="row">
          <div
            class="
              col-12 col-lg-3
              d-flex
              align-items-center
              flex-column
              d-lg-block
            "
          >
            <h5 class="text-grey text-uppercase">Come find us</h5>
            <ul>
              <li>
                <a href="#" class="text-grey">
                  <span class="text-grey"
                    >12345 North Main Street New York, NY 5555555
                  </span>
                </a>
              </li>
              <li>
                <span class="text-grey">Phone:</span>
                <a href="#" class="text-white"> 1.800.555.6789</a>
              </li>
              <li>
                <span class="text-grey">Email:</span>
                <a href="#" class="text-white"> info@your-domain.com</a>
              </li>
            </ul>
          </div>
          <div
            class="
              col-12 col-lg-3
              d-flex
              align-items-center
              flex-column
              d-lg-block
            "
          >
            <h5 class="text-grey text-uppercase">Recent posts</h5>
            <ul>
              <li>
                <a href="#">
                  <i class="fa-solid fa-chevron-right fa-xs"></i>
                  Train with free weights or your body weight?
                </a>
              </li>
              <li>
                <a href="#">
                  <i class="fa-solid fa-chevron-right fa-xs"></i>
                  Nutritional advice that will keep you training</a
                >
              </li>
            </ul>
          </div>
          <div
            class="
              col-12 col-lg-3
              d-flex
              align-items-center
              flex-column
              d-lg-block
              text-grey
              lh-lg
            "
          >
            <h5 class="text-grey text-uppercase">Opening times</h5>
            <ul>
              <li>
                <span>Weekdays Monday- Friday</span> <br />
                <span>09:00 - 19:00</span>
              </li>
              <li>
                <span>Weekdays Saturday- Sunday</span> <br />
                <span>09:00 - 21:00</span>
              </li>
            </ul>
          </div>
          <div
            class="
              col-12 col-lg-3
              d-flex
              align-items-center
              flex-column
              d-lg-block
            "
          >
            <figure>
              <img
                src="../assets/img/gym_ad-compressor.jpg"
                alt="discount"
                class="img-fluid scale"
              />
            </figure>
          </div>
        </div>
      </div>
    </section>
    <!-- Bottom Footer -->
    <section id="bottom-footer">
      <div class="container-fluid pt-5 bs-black">
        <div class="container">
          <div class="row align-items-center">
            <div class="col-12 col-lg-8 text-white">
              © Copyright 2022 | Class52 by <a href="#">Boolean</a>| All Rights
              Reserved | Powered by <a href="#">Vuejs</a>
            </div>
            <div
              class="col-12 offset-lg-0 col-lg-4 d-flex justify-content-lg-end"
            >
              <SocialIcons
                :social-list="socialList"
                :not-social="false"
                :isPink="true"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Btn from "./Btn.vue";
import SocialIcons from "./SocialIcons.vue";
export default {
  name: "Footer",
  components: {
    Btn,
    SocialIcons,
  },
  data() {
    return {
      socialList: [
        { name: "fa-facebook-f" },
        { name: "fa-twitter" },
        { name: "fa-instagram" },
        { name: "fa-youtube" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_mixin.scss";
#top-footer {
  background-image: url("../assets/img/home-parallax.jpg");
  background-attachment: fixed;
}
#main-footer {
  ul {
    list-style-type: none;
    padding-left: 0;
    a {
      text-decoration: none;
      line-height: 2rem;
      color: #fff;
    }
  }
}

#bottom-footer {
  a {
    text-decoration: none;
    color: #fff;
  }
}

img.scale:hover {
  @include scale(1.2);
}
</style>