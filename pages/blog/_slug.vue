<template>
  <article>
    <div class="container mx-auto lg:max-w-screen-lg">
      <div class="w-full h-96 overflow-hidden rounded-2xl">
        <img
          v-if="article.img"
          class="h-full w-full object-cover"
          :src="article.img"
          :alt="article.alt"
        />
      </div>
      <nuxt-content :document="article" />
    </div>
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()
    return {
      article,
    }
  },
}
</script>
