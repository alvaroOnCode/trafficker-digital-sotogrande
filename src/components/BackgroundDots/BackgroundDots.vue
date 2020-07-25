<template>
  <div class="background-dots-container">
    <div v-for="(n, i) in 4" :key="`d1-${i}`" class="dot dot-depth-1"></div>
    <div v-for="(n, i) in 8" :key="`d2-${i}`" class="dot dot-depth-2"></div>
    <div v-for="(n, i) in 10" :key="`d3-${i}`" class="dot dot-depth-3"></div>
  </div>
</template>

<script>
export default {
  name: "BackgroundDots",
  methods: {
    mouseParallax(e, elem) {
      const _w = window.innerWidth / 2;
      const _h = window.innerHeight / 2;

      const _mouseX = e.clientX;
      const _mouseY = e.clientY;

      const _depth1 = `${50 - (_mouseX - _w) * 0.025}%, ${50 -
        (_mouseY - _h) * 0.025}%`;
      const _depth2 = `${50 - (_mouseX - _w) * 0.05}%, ${50 -
        (_mouseY - _h) * 0.05}%`;
      const _depth3 = `${50 - (_mouseX - _w) * 0.75}%, ${50 -
        (_mouseY - _h) * 0.75}%`;

      if (elem.classList.contains("dot-depth-1")) {
        elem.style.transform = `translate(${_depth3})`;
      }

      if (elem.classList.contains("dot-depth-2")) {
        elem.style.transform = `translate(${_depth2})`;
      }

      if (elem.classList.contains("dot-depth-3")) {
        elem.style.transform = `translate(${_depth1})`;
      }
    }
  },
  mounted() {
    const dots = Array.from(document.querySelectorAll(".dot"));

    dots.forEach(dot => {
      dot.style.left = `${Math.random() * (100 - 0) + 0}%`;
      dot.style.top = `${Math.random() * (100 - 0) + 0}%`;
    });

    window.addEventListener("mousemove", event => {
      dots.forEach(dot => {
        this.mouseParallax(event, dot);
      });
    });
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";
@import "./backgroundDots.scss";
</style>
