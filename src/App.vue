<template>
  <div id="app">
    <a-layout>
      <!-- Header -->
      <a-layout-header id="main-header">
        <Header />
      </a-layout-header>

      <!-- Content -->
      <a-layout-content id="main-content">
        <router-view />
      </a-layout-content>

      <!-- Footer -->
      <a-layout-footer id="main-footer">
        <Footer />
      </a-layout-footer>
    </a-layout>
  </div>
</template>

<script>
import Footer from "./layout/Footer/Footer";
import Header from "./layout/Header/Header";

export default {
  components: {
    Footer,
    Header
  }
};
</script>

<style lang="scss">
@import "./assets/scss/main.scss";
</style>
