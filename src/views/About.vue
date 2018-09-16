<template>
  <section>
    <p>At {{ age || 1 }} years old I’m looking forward to everything we will accomplish.</p>
    <p>Passionate Developer.<br>Quick Learner.<br>Cheerful Human.</p>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';
import { Component, Prop } from 'vue-property-decorator';

@Component
export default class About extends Vue {
  private get age() {
    return Math.floor(
      (new Date().getTime() - new Date('1995-01-05').getTime()) /
        (1000 * 60 * 60 * 24 * 365),
    );
  }
}
</script>


<style lang="stylus" scoped>
section
  color white
  display flex
  flex-flow column
  font-size 1.5rem
  margin-top 5rem
  max-width 500px

p
  margin 2rem
  text-align center
  &:first-child
    margin-top 0
</style>
