<template>
  <Select name='tagFilter' :value={this.props.selectedTags} options={options} onChange={this.props.onChange} multi autoBlur />
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'

@Component
export default class Filter extends Vue {
  @Prop tagList!: string[]
  @Prop selectedTags!: string[]
  @Prop onChange: ()=>void
}

</script>