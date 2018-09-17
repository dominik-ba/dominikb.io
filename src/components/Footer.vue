<template>
  <footer>
    <ul>
      <li>Made with ❤️ in Austria.</li>
      <li>(c) {{ currentYear }} - Dominik Bauernfeind</li>
      <li>Icons by <a href="https://icons8.de/" target="_blank">icons8</a>.</li>
    </ul>
  </footer>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

@Component
export default class Footer extends Vue {
  protected currentYear = new Date().getUTCFullYear();
}
</script>

<style lang="stylus" scoped>
footer
  background-color lightgrey
  display flex
  height 6rem
  justify-content center
  margin-top 3rem
  width 100%

ul
  align-items center
  display flex
  flex-flow column
  flex-grow 1
  height 100%
  justify-content space-evenly
  list-style none
  margin 0 3rem
  max-width pagewrapper

li span
  color

a
  color inherit

@media (min-width: w_tablet)
  footer
    height 2rem

  ul
    flex-flow row
    justify-content space-between
</style>
