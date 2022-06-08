<template>
  <article>
    <div class="container mx-auto lg:max-w-screen-md p-2">
      <header>
        <div class="flex pt-16">
          <div class="flex flex-col my-auto w-full h-4/6">
            <h2 class="text-4xl font-bold p-8 pl-0.5">{{ article.title }}</h2>
            <div class="overflow-hidden max-h-screen rounded-2xl">
              <img
                v-if="article.img"
                class="h-full w-full object-cover"
                :src="article.img"
                :alt="article.alt"
              />
            </div>
          </div>
        </div>
      </header>
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
