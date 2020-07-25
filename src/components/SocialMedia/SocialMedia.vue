<template>
  <div :class="`social-media-container ${align}`">
    <a href="#">
      <a-icon type="facebook" />
    </a>

    <a href="#">
      <a-icon type="instagram" />
    </a>
    <a href="#">
      <a-icon type="linkedin" />
    </a>
    <a href="#">
      <a-icon type="twitter" />
    </a>
  </div>
</template>

<script>
export default {
  name: "SocialMedia",
  props: {
    align: {
      type: String,
      default: "center"
    }
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./socialMedia.scss";
</style>