<template>
  <Header></Header>

  <div class="titles-container">
    <h1 class="first-title">CanSat 2020-2021</h1>
    <h1 class="second-title">Oli 3AI Group</h1>

    <div class="button-container">
      
    </div>
  </div>

</template>

<script>
import Header from "./components/Header";
import LinkButton from "./components/LinkButton";
import anime from "animejs/lib/anime.es.js";
import "./styles/fonts.sass";

export default {
  name: "App",
  components: {
    Header,
  },
  mounted() {

    anime({
      targets: ".first-title",
      translateY: {
        value: [-250, 0],
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


.button-container
  display: inline-block

  a
    color: #202020
    text-decoration: none

    :visited
      color: #202020

  .inner-button
    display: flex
    align-items: center
    border-radius: 1rem
    padding: 1rem 0.6rem
    cursor: pointer

    box-shadow: 0px 0px 5px 1px rgba(130, 130, 130, 0.18)

  .button-text
    font-family: $font-family
    font-weight: 700
    font-size: 1.3rem
    margin-top: 1px

  img
    width: 2.5em
    height: 2.5rem

  .button-text, img
    margin: 0rem 1rem

  .texts-container
    text-align: left
</style>
