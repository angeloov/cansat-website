<template>
  <div>
    <ul class="header-links">
      <li>
        <a target="_blank" href="https://www.esero.it/cansat/" class="link">What is CanSat?</a>
      </li>
      <li>
        <a target="_blank" href="https://www.istitutoolivetti.it/" class="link">Our school</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>

$font-family: Gilroy, "Helvetica Neue", Helvetica, Arial, sans-serif

.header-links
  color: #202020
  list-style: none

  display: flex
  justify-content: center

  margin-top: 2rem

  font-family: $font-family
  font-weight: 600
  font-size: 1.2rem

  li
    margin: 0 1rem

.link
  color: #202020
  text-decoration: none

  :visited
    color: #202020
</style>
