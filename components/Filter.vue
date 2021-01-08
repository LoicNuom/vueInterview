<template>
  <v-select multiple :options="tagList" :value="selectedTags" @input="onChange"/>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'

@Component
export default class Filter extends Vue {
  @Prop() tagList!: string[]
  @Prop() selectedTags!: string[]
  @Prop() onChange!: ()=>void

}

</script>