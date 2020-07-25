<template>
  <div class="subservice-container">
    <h3 class="subservice-title">
      <a-icon :type="subservice.iconType" />
      {{ subservice.title }}
    </h3>

    <p class="subservice-desc">{{ subservice.description }}</p>
  </div>
</template>

<script>
export default {
  name: "Subservice",
  props: ["subservice"]
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./subservice.scss";
</style>
