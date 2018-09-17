<template>
  <section>
    <p>I started out as a professional developer <span class="strike-through">about</span> {{ yearsAsDev}} years ago, after having been a hobbiest long before.</p>
    <p>My main proficiency lies with PHP and Laravel, as well as everything related to Javascript</p>
    <p>I love building APIs and services for others to use and really enable their full potential.</p>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import { Prop, Provide, Watch } from 'vue-property-decorator';
import { setInterval } from 'timers';

@Component
export default class Work extends Vue {
  @Provide() private start: Date = new Date('2017-08-02');
  @Provide() private now: Date = new Date();

  get yearsAsDev() {
    return (
      (this.now.getTime() - this.start.getTime()) / (1000 * 60 * 60 * 24 * 365)
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
  max-width 600px

p
  margin 2rem
  text-align center
  &:first-child
    margin-top 0

.strike-through
  text-decoration line-through

</style>
