<template>
  <section>
    <section className="hero">
      <div className="hero-body">
        <div className="container">
          <h1 className="title">The Great Article Database</h1>
        </div>
      </div>
    </section>
    <section class="">
      <h2 class="">Filter by tag:</h2>
      <Filter
        :onChange="handleFilterChange"
        :tagList="tagList"
        v-model="selectedTags"
      />
    </section>
    <section class="">
      <!-- TODO: Create a list of the cards, the list has to be reactive -->
      <div class="flex flex-row">
        <ArticleCard />
      </div>
    </section>
  </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator';
import { getAllTags } from '../mockAPI/allTags';

@Component
export default class IndexPage extends Vue {
  articles: any = [];
  tagList: string[] = [];
  selectedTags: [] = [];

  handleFilterChange() {
    /* TODO: update the selected tag list */
  }

  async created() {
    this.tagList = await getAllTags();
    /*TODO: get list of Articles from Database */
  }
}
</script>

