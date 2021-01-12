<template>
  <div class="page2">
    <div class="partecipants-container">
      <div class="partecipants-inner">
        <div class="top-line"></div>
        <h1 class="partecipants-title">Partecipants</h1>
      </div>
      <span class="shadows">
        <div class="blurred-shadow blue-blur"></div>
        <div class="blurred-shadow yellow-blur"></div>
        <div class="blurred-shadow purple-blur"></div>
      </span>
    </div>

    <div class="partecipants-links">
      <NameCard name="Cristian Alasotto" link="https://github.com/CristianAlasotto"></NameCard>
      <NameCard name="Angelo Voicu" link="https://github.com/angeloov"></NameCard>
      <NameCard name="Andrea Bertarione" link="https://github.com/kirito012"></NameCard>
      <NameCard name="Matteo Orefice" link="https://github.com/Prodigi14"></NameCard>
    </div>

    <Footer></Footer>
  </div>
</template>

<script>
import NameCard from "../components/NameCard";
import Footer from "../components/Footer";
import anime from "animejs/lib/anime.es.js";

export default {
  name: "Page2",
  components: {
    NameCard,
    Footer,
  },
  mounted() {
    let animationDone = false;

    const observer = new IntersectionObserver(
      entries => {
        if (entries[0].isIntersecting === true && !animationDone) {
          anime({
            targets: ".blurred-shadow",
            opacity: {
              value: [0, 1],
              duration: 1800,
            },
            easing: "easeInOutExpo",
          });

          animationDone = true;
        }
      },
      { threshold: [1] }
    );

    observer.observe(document.querySelector(".shadows"));
  },
};
</script>

<style lang="sass">

$font-family: Gilroy, "Helvetica Neue", Helvetica, Arial, sans-serif

.page2
  margin-top: 14rem
  position: relative

.partecipants-container
  position: relative
  top: 40%
  left: 8%
  transform: translate(0, -50%)

  width: 30rem
  height: 30rem

.blurred-shadow
  border-radius: 100%
  filter: blur(20px)
  background-blend-mode: multiply
  position: absolute

  z-index: -1

.yellow-blur
  background: radial-gradient(50% 50% at 50% 50%, rgba(252, 181, 0, 0.4) 0%, rgba(255, 255, 255, 0) 100%)

  width: 260px
  height: 260px

  left: -8%
  top: 30%
  tranform: translate(0, -50%)

.blue-blur
  background: radial-gradient(50% 50% at 50% 50%, rgba(3, 112, 251, 0.5) 0%, rgba(255, 255, 255, 0) 100%)

  width: 480px
  height: 480px

  left: 10%
  top: 5%

.purple-blur
  background: radial-gradient(50% 50% at 50% 50%, #DCC1E4 0%, rgba(255, 255, 255, 0) 100%, rgba(255, 255, 255, 0) 100%)

  width: 230px
  height: 230px

  left: 30%
  top: 55%
  transform: translate(-50%)

.partecipants-inner
  position: absolute
  top: 50%

.partecipants-title
  font-size: 3.8rem
  font-family: $font-family

  color: #202020

  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-rendering: optimizeLegibility

  margin: 0

.top-line
  width: 3rem
  height: 0.4rem

  background: #202020
  border-radius: 5rem

.partecipants-links
  display: flex
  flex-direction: column

  position: absolute
  top: 5%
  right: 10%
  transform: translate(0, -50%)

[data-aos="shadow"]
  opacity: 0
  transition-property: opacity

  &.aos-animate
    opacity: 1
</style>
