<template>
  <div class="home-container">
    <!-- <BackgroundDots /> -->

    <div class="home-container_squares">
      <SquaresContainer />
    </div>

    <div class="home-container_subservices">
      <HomeServices />
    </div>

    <div class="home-container_sobre-nosotros">
      <HomeSobreNosotros />
    </div>
  </div>
</template>

<script>
// import BackgroundDots from "../../components/BackgroundDots/BackgroundDots";
import HomeServices from "../../components/HomeServices/HomeServices";
import HomeSobreNosotros from "../../components/HomeSobreNosotros/HomeSobreNosotros";
import SquaresContainer from "../../components/SquaresContainer/SquaresContainer";

export default {
  name: "Home",
  components: {
    // BackgroundDots,
    HomeServices,
    HomeSobreNosotros,
    SquaresContainer
  },

  head() {
    return {
      title: "Álvaro Saavedra Díaz 🧑‍💻 Software Developer",
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content:
            "Página web de Álvaro Saavedra (@alvaroOnCode), donde encontrarás información personal, profesional y artículos de desarrollo de software."
        }
      ]
    };
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./home.scss";
</style>
