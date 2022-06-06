<template>
  <div class="container lg:max-w-screen-lg mx-auto px-12 lg:px-0">
    <BigArticleCard :article="articles[0]" />
    <ul class="flex flex-wrap">
      <li
        v-for="article of articles.slice(1)"
        :key="article.slug"
        class="xs:w-full md:w-1/2 px-2 xs:mb-6 md:mb-12 article-card"
      >
        <ArticleCard :article="article" />
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'IndexPage',
  async asyncData({ $content }) {
    const articles = await $content('articles')
      .only(['title', 'description', 'img', 'slug', 'author', 'createdAt'])
      .sortBy('createdAt', 'desc')
      .fetch()
    // const tags = await $content('tags')
    //   .only(['name', 'description', 'img', 'slug'])
    //   .sortBy('createdAt', 'asc')
    //   .fetch()
    return {
      articles,
      // tags,
    }
  },
})
</script>
