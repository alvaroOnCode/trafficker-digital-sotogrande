<template>
  <div class="home-services-container">
    <a-row class="home-services_row" type="flex" justify="start">
      <a-col
        v-for="(subservice, i) in subservices"
        :key="`subservice-${i}`"
        :span="6"
        class="home-services_col"
      >
        <Subservice :subservice="subservice" />
      </a-col>
    </a-row>
  </div>
</template>

<script>
// Data
import { subservices } from "../../data/subservices.js";

// Components
import Subservice from "../../components/Subservice/Subservice";

export default {
  name: "HomeServices",
  components: {
    Subservice
  },
  data: () => ({
    subservices
  })
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./homeServices.scss";
</style>
