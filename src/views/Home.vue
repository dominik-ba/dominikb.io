<template>
  <section>
    <figure>
      <img src="../assets/me.jpg" alt="Dominik">
    </figure>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from '@/components/Navbar.vue';

@Component({
  components: {
    Navbar,
  },
})
export default class Home extends Vue {}
</script>

<style lang="stylus" scoped>
figure
  border-radius 5px
  height 40vh
  overflow hidden

img
  height 100%
</style>

