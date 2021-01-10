<template>
  <Page1></Page1>
  <Page2></Page2>
</template>

<script>
import Page1 from "./pages/Page1";
import Page2 from "./pages/Page2";
import anime from "animejs/lib/anime.es.js";
import "./styles/fonts.sass";

export default {
  name: "App",
  components: {
    Page1,
    Page2,
  },
  mounted() {
    anime({
      targets: ".title",
      translateY: {
        value: [-400, 0],
        duration: 1300,
      },
      easing: "easeInOutExpo",
    });

    anime({
      targets: ".header-links",
      delay: 1200,
      opacity: {
        value: [0, 1],
        duration: 500,
      },
      easing: "easeInCubic",
    });
  },
};
</script>

<style lang="sass"></style>
