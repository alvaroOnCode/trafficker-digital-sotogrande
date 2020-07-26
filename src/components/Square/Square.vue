<template>
  <div class="square-container">
    <h2>{{ title }}</h2>
  </div>
</template>

<script>
export default {
  name: "Square",
  props: {
    title: {
      type: String,
      default: ""
    }
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./square.scss";
</style>
