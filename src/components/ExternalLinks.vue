<template>
  <section class="third-party-links">
    <a href="mailto:bauernfeind.dominik@gmail.com">
      <Icon src="gmail.svg" alt="Alt text"/>
    </a>
    <a href="https://github.com/dominik-ba">
      <Icon src="github.svg" alt="Alt text"/>
    </a>
    <a href="https://www.xing.com/profile/Dominik_Bauernfeind2">
      <Icon src="xing.svg" alt="Alt text"/>
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
