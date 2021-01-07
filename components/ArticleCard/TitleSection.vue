<template>
  <div class="">
    <p class="txt-lg">
      Title <!-- TODO Replace with the title from the prop -->
    </p>
    <div class="flex flex-row m-2">
        <!-- TODO show the list of tags using v-for -->
    </div>
    
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'

@Component
export default class LoginPage extends Vue {
  @Prop tags!: string[]
  @Prop title!: string
}

</script>