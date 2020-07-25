<template>
  <div class="footer-copyright-container">
    <p>
      &copy; {{ year }} Trafficker Digital Sotogrande&nbsp;|&nbsp;Hecho con&nbsp;
      <a-icon class="footer__icon-heart" type="heart" />&nbsp;por&nbsp;
      <a href="https://alvarosaavedradiaz.com/">Álvaro Saavedra Díaz</a>
    </p>
  </div>
</template>

<script>
export default {
  name: "FooterCopyright",
  computed: {
    year: () => {
      const d = new Date();
      return d.getFullYear();
    }
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./footerCopyright.scss";
</style>
