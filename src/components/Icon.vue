<template>
  <figure>
    <img :src="require('../assets/' + src)" :alt="alt">
  </figure>
</template>

<script lang="ts">
import { Prop, Vue, Component } from 'vue-property-decorator';

@Component
export default class Icon extends Vue {
  @Prop({ required: true })
  public src!: string;
  @Prop({ required: true })
  public alt!: string;
}
</script>

<style lang="stylus" scoped>
figure
  height 50px
  width 50px

img
  height 100%
  width 100%
</style>
