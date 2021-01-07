<template>

  <li class="col-span-1 bg-white rounded-lg shadow divide-y divide-gray-200" @click="handleClick">
      <div class="w-full flex flex-row items-center justify-between p-6 space-x-6">
        <div class="grid grid-cols-3">
          <div class="">
            <figure class="w-6/12 px-4">
              <!-- TODO:  show the image -->
              <img src='imageUrl' alt="Image Description" />
            </figure>
          </div>
          <div class="col-span-2">
            <!-- TODO: pass the article details (title and tags) -->
            <TitleSection :title="Article Title" :tags="[]"/>
          </div>
        </div>
        <div class="text-base font-light leading-relaxed mt-0 mb-4 text-gray-800">
          <!-- TODO: Pass the article text and the max length. Max length can be taken from a config or to be respond to size -->
          <Summary text='Article text' :maxLength='150'/>
        </div>
      </div>
    </li>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'

@Component
export default class ArticleCard extends Vue {
  @Prop() id!: string
  @Prop() title!: string
  @Prop() tags!: string[]
  @Prop() summary!: string
  @Prop() imageUrl!: string

  handleClick(){
    /* TODO: Go to the article page on click, you should use Vue Router*/
    // use this.$router to get the Vue Router (https://router.vuejs.org/guide/essentials/navigation.html)
  }
}

</script>