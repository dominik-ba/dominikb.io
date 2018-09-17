<template>
  <nav id="nav">
      <router-link to="/about">About</router-link>
      <router-link to="/work">Work</router-link>
      <router-link to="/contact">Contact</router-link>
    </nav>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Navbar extends Vue {}
</script>

<style lang="stylus" scoped>
nav
  display flex
  justify-content space-between

  a
    color white
    font-size 1.5rem
    text-decoration none

    &.router-link-exact-active
      font-size 2rem
</style>
