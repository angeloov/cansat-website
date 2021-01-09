<template>
  <span>
    <a href="https://github.com/angeloov/cansat-2021" target="_blank">
      <span class="inner-button">
        <span class="texts-container">
          <p class="button-text">View our project</p>
          <p class="button-text">on GitHub</p>
        </span>
        <img :src="require('../assets/open-link.png')" alt="Open link icon" />
      </span>
    </a>
  </span>
</template>

<script>
export default {
  name: "GithubButton",
};
</script>

<style lang="sass">
$font-family: Gilroy, "Helvetica Neue", Helvetica, Arial, sans-serif

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
