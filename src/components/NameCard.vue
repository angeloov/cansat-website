<template>
  <a :href="link" target="_blank" class="link">
    <div class="partecipant-card">
      <p class="partecipant-name">
        {{ name }}
      </p>
      <img
        class="left-arrow-icon"
        :src="require('../assets/left-arrow-icon.svg')"
        alt="Left arrow icon"
      />
    </div>
  </a>
</template>

<script>
export default {
  name: "NameCard",
  props: {
    name: String,
    link: String,
  },
};
</script>

<style lang="sass">

$font-family: Gilroy, "Helvetica Neue", Helvetica, Arial, sans-serif

.partecipant-card
  border-radius: 10px

  margin: 0.5rem
  padding: 1rem 1.5rem

  background: #FFFFFF

  display: inline-flex
  justify-content: center
  align-items: center

  box-shadow: 0px 2px 4px rgba(130, 130, 130, 0.3)

  .partecipant-name
    width: 15rem
    font-size: 1.5rem
    font-family: Montserrat, Gilroy, "Helvetica Neue", Helvetica, Arial, sans-serif
    font-weight: 500
    margin: 0

.left-arrow-icon
  margin-left: 1.2rem
  width: 1.5rem
  height: 1.5rem

.link
  color: #202020
  text-decoration: none

  :visited
    color: #202020
</style>
