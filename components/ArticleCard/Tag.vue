<template>
  <span class="flex">
    {{ tag }}
  </span>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator';

@Component
export default class LoginPage extends Vue {
  @Prop tag!: string;
}
</script>