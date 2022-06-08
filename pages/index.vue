<template>
  <div class="container lg:max-w-screen-lg mx-auto px-12 lg:px-0">
    <BigArticleCard v-show="!isMobileWidth" :article="articles[0]" />
    <div v-show="isMobileWidth" class="pt-24 mb-6 md:mb-12 px-2">
      <ArticleCard :article="articles[0]" />
    </div>
    <ul class="flex flex-wrap">
      <li
        v-for="article of articles.slice(1)"
        :key="article.slug"
        class="w-full md:w-1/2 px-2 mb-6 md:mb-12"
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
    return {
      articles,
    }
  },
  data() {
    if (process.client) {
      return {
        isMobileWidth: !!(document.documentElement.clientWidth < 768),
      }
    } else {
      return { isMobileWidth: null }
    }
  },
  mounted() {
    window.onresize = () => {
      this.isMobileWidth = !!(document.documentElement.clientWidth < 768)
    }
  },
})
</script>
