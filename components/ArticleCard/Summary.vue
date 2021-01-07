<template>
  <p class="">
    <!-- TODO: Show the summary of the Article by cutting it at the maxLength. We recommend to use the Truncate Function from lodash -->
  </p>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'

@Component
export default class LoginPage extends Vue {
  @Prop text!: string
  @Prop maxLength!: number
}

</script>