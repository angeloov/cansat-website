<template>
  <Header></Header>

  <div class="titles-container">
    <h1 class="first-title title">CanSat 2020-2021</h1>
    <h1 class="first-title shadow-first-title title">CanSat 2020-2021</h1>
    <h1 class="second-title title">Oli 3AI Group</h1>

    <div class="button-container">
      <GithubButton></GithubButton>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import GithubButton from "./components/GithubButton";
import anime from "animejs/lib/anime.es.js";
import "./styles/fonts.sass";

export default {
  name: "App",
  components: {
    Header,
    GithubButton,
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

<style lang="sass">
$font-family: Gilroy, "Helvetica Neue", Helvetica, Arial, sans-serif

body
  margin: 0

  background-image: url("./assets/shapes-background.svg")
  background-repeat: no-repeat
  background-size: 80%
  background-position: center

  min-height: 100vh


.titles-container
  position: absolute
  left: 50%
  top: 50%
  transform: translate(-50%, -50%)

  text-align: center


.first-title
  background: linear-gradient(268.23deg, #0370FB 19.37%, #D800DC 69.49%)
  background-clip: text

  -webkit-background-clip: text
  -webkit-text-fill-color: transparent
  --moz-background-clip: text
  font-family: $font-family

  font-size: 3.8rem
  font-weight: 800

  filter: saturate(1.2)

  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-rendering: optimizeLegibility

  text-shadow: rgba(0,0,0,.01) 0 0 1px
  margin: 0

  position: relative

.shadow-first-title
  position: absolute
  top: 0

  opacity: 0.20
  filter: blur(8px)
  z-index: -1


.second-title
  font-size: 2.5rem
  font-weight: 700

  color: #202020

  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-rendering: optimizeLegibility

  font-family: $font-family

  margin-top: 0.8rem
  margin-bottom: 2.5rem
</style>
