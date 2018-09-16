<template>
  <div id="app">
    <router-link to="/">
      <Header id="header"/>
    </router-link>
    <Navbar id="nav"/>
    <router-view id="content"/>
    <ExternalLinks/>
    <Footer id="footer"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';
import Header from '@/components/Header.vue';
import ExternalLinks from '@/components/ExternalLinks.vue';

@Component({
  components: {
    Navbar,
    Footer,
    Header,
    ExternalLinks,
  },
})
export default class App extends Vue {
  public comments: true;
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Overpass+Mono:400,700');
</style>

<style lang="stylus">
*
  box-sizing border-box
  margin 0
  padding 0

html,body
  font-size fontsize

#app
  align-items center
  display flex
  flex-flow column
  font-family 'Overpass Mono', 'monospace'
  min-height 100vh
  overflow hidden
  position relative

  &:before
    background darkgrey
    bottom 0
    content ''
    left 0
    position absolute
    right 0
    top 0
    z-index -2

  &:after
    background url('assets/crissxcross.png') repeat
    bottom 0
    content ''
    left 0
    opacity .65
    position absolute
    right 0
    top 0
    z-index -1

#header
  position relative

#nav
  max-width 80vw
  padding-top 3rem
  position relative
  width 100%

#content
  flex-grow 1
  margin-top 2rem

@media(min-width: w_phone)
  #nav
      max-width 70vw

@media(min-width: w_phone_xl)
  #nav
      max-width 60vw
  #content
      margin-top 3rem

@media(min-width: w_tablet)
  #app
    padding-top 3rem
  #nav
      max-width 50vw
  #content
      margin-top 5rem

@media(min-width: w_desktop)
  #nav
      max-width 40vw
  #content
      margin-top 8rem
</style>