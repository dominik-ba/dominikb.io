<template>
  <section class="third-party-links">
    <a href="mailto:bauernfeind.dominik@gmail.com">
      <Icon src="gmail.svg" alt="Gmail"/>
    </a>
    <a href="https://github.com/dominikb">
      <Icon src="github.svg" alt="Github"/>
    </a>
    <a href="https://twitter.com/dominik_ba">
      <Icon src="twitter.svg" alt="Twitter"/>
    </a>
    <a href="https://www.xing.com/profile/Dominik_Bauernfeind2">
      <Icon src="xing.svg" alt="Xing"/>
    </a>
  </section>
</template>

<script lang="ts">
import { Prop, Vue, Component } from 'vue-property-decorator';
import Icon from '@/components/Icon.vue';

@Component({
  components: { Icon },
})
export default class ExternalLinks extends Vue {}
</script>

<style lang="stylus" scoped>
.third-party-links
  background-color lightgrey
  border-radius 500px
  display flex
  justify-content space-around
  padding 0 1rem
  width 250px
</style>
