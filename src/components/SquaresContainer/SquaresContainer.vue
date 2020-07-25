<template>
  <div class="squares-container-container">
    <h3>Nuestros servicios</h3>

    <a-row class="squares-container_row">
      <a-col class="squares-container_col" :span="4" :style="style">
        <Square :category="'marketingDigital'" />
      </a-col>

      <a-col class="squares-container_col" :span="4" :style="style">
        <Square :category="'desarrolloWeb'" />
      </a-col>

      <a-col class="squares-container_col" :span="4" :style="style">
        <Square :category="'diseno'" />
      </a-col>

      <a-col class="squares-container_col" :span="4" :style="style">
        <Square :category="'produccionAudiovisual'" />
      </a-col>

      <a-col class="squares-container_col" :span="4" :style="style">
        <Square :category="'fotografia'" />
      </a-col>

      <a-col class="squares-container_col" :span="4" :style="style">
        <Square :category="'packs'" />
      </a-col>
    </a-row>
  </div>
</template>

<script>
import Square from "../../components/Square/Square";

export default {
  name: "SquaresContainer",
  data: () => ({
    columnHeight: {
      type: Number,
      default: 16
    }
  }),
  components: {
    Square
  },
  computed: {
    style() {
      return `height: ${this.columnHeight}px`;
    }
  },
  methods: {
    calcColumnHeight() {
      this.columnHeight = document.querySelector(
        ".squares-container_col"
      ).clientWidth;
    }
  },
  mounted() {
    this.calcColumnHeight();
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./squaresContainer.scss";
</style>
