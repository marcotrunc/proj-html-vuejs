<template>
  <div>
    <section id="top-footer" class="py-7">
      <div class="container-fluid">
        <div class="container">
          <div class="row text-white align-items-center">
            <div class="col-10">
              <div>
                <h3>Achieve Your Fitness Goals</h3>
                <span class="fs-5">
                  Flexible membership packages to suit alla levels of athelete
                  and achive your fitness goals
                </span>
              </div>
            </div>
            <div class="col-2">
              <Btn textBtn="Join us" class="w-100" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="main-footer">
      <div class="container py-7">
        <div class="row">
          <div class="col-3">
            <h5 class="text-grey text-uppercase">Come find us</h5>
            <ul>
              <li>
                <a href="#" class="text-grey"
                  >12345 North Main Street New York, NY 5555555
                </a>
              </li>
              <li>
                <span class="text-grey">Phone:</span>
                <a href="#" class="text-white">1.800.555.6789</a>
              </li>
              <li>
                <span class="text-grey">Email:</span>
                <a href="#" class="text-white">info@your-domain.com</a>
              </li>
            </ul>
          </div>
          <div class="col-3">
            <h5 class="text-grey text-uppercase">Recent posts</h5>
            <ul>
              <li>
                <a href="#">> Train with free weights or your body weight? </a>
              </li>
              <li>
                <a href="#">> Nutritional advice that will keep you training</a>
              </li>
            </ul>
          </div>
          <div class="col-3 text-grey lh-lg">
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
          <div class="col-3">
            <figure>
              <img
                src="../assets/img/gym_ad-compressor.jpg"
                alt="discount"
                class="img-fluid"
              />
            </figure>
          </div>
        </div>
      </div>
    </section>
    <section id="bottom-footer">
      <div class="container-fluid pt-5">
        <div class="container">
          <div class="row align-items-center">
            <div class="col-8 text-white">
              © Copyright 2022 | Class52 by <a href="#">Boolean</a>| All Rights
              Reserved | Powered by <a href="#">Vuejs</a>
            </div>
            <div class="col-4 d-flex justify-content-end">
              <SocialIcons
                :social-list="socialList"
                :not-social="false"
                :bg-col="true"
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
#top-footer {
  background-image: url("../assets/img/home-parallax.jpg");
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
</style>