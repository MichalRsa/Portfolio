<template>
  <div class="flex h-screen">
    <NuxtLink
      :to="{ name: 'blog-slug', params: { slug: article.slug } }"
      class="flex flex-row container md:h-96 h-64 max-w-6xl my-auto"
    >
      <div class="w-7/12 overflow-hidden rounded-2xl">
        <img
          v-if="article.img"
          class="h-full w-full object-cover"
          :src="article.img"
        />
      </div>
      <div class="flex justify flex-col p-8 w-5/12">
        <p class="text-xs font-thin pb-8">{{ article.createdAt }}</p>
        <h2 class="text-4xl font-bold pb-8">{{ article.title }}</h2>
        <p class="test-base font-light pb-8">{{ article.description }}</p>
      </div>
    </NuxtLink>
  </div>
</template>
<script>
export default {
  props: {
    article: { type: Object, default: () => {} },
  },
}
</script>
