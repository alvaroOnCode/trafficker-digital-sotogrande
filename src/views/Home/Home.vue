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
  metaInfo: {
    title: "Trafficker Digital Sotogrande",
    titleTemplate: "%s - 📊 ¡Hola!",
    htmlAttrs: {
      lang: "en",
      amp: true
    }
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./home.scss";
</style>
