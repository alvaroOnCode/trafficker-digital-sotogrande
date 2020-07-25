<template>
  <div class="square-container">
    <h2>{{ title }}</h2>
  </div>
</template>

<script>
import { squares } from "../../data/squares.js";

export default {
  name: "Square",
  data: () => ({
    squares
  }),
  props: {
    category: {
      type: String,
      default: ""
    }
  },
  computed: {
    title() {
      const t =
        this.category && squares[this.category]
          ? squares[this.category].title
          : "Error";
      return t;
    }
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./square.scss";
</style>
