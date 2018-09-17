<template>
<header>
<h1>Dominik Bauernfeind</h1>
</header>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

@Component
export default class Header extends Vue {}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Bangers');
</style>

<style lang="stylus" scoped>
header
  display inline-block
  margin-bottom 1rem
  padding 4.5rem .5rem .5rem

h1
  border-bottom 2px solid white
  color white
  display inline
  font-family 'Bangers', 'cursive'
  font-size 2rem
  letter-spacing 5px
  padding 1rem
  text-shadow 2rem (-@font-size) turquoise

@media (min-width: w_phone)
  h1
    font-size 2.5rem
    letter-spacing 8px
    text-shadow 2rem (-@font-size) turquoise

@media (min-width: w_phone_xl)
  h1
    font-size 3rem
    letter-spacing 13px
    text-shadow 2rem (-@font-size) turquoise

@media (min-width: w_tablet)
  h1
    font-size 3.5rem
    letter-spacing 15px
    text-shadow 2rem (-@font-size) turquoise

@media (min-width: w_desktop)
  h1
    font-size 4rem
    letter-spacing 20px
    text-shadow 2rem (-@font-size) turquoise

</style>
