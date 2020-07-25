<template>
  <div class="header-container">
    <!-- Social Media -->
    <div class="header_social-media">
      <SocialMedia :align="'right'" />
    </div>

    <!-- Logo -->
    <div class="header_logo">
      <Logo :size="'medium'" />
    </div>

    <!-- Dots
    <div class="header_dots">
      <div class="header_dot header_dot--1"></div>
      <div class="header_dot header_dot--2"></div>
    </div>-->
  </div>
</template>

<script>
import Logo from "../../components/Logo/Logo";
import SocialMedia from "../../components/SocialMedia/SocialMedia";

export default {
  name: "Header",
  components: {
    Logo,
    SocialMedia
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./header.scss";
</style>
