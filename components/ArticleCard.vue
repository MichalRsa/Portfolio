<template>
  <NuxtLink
    :to="{ name: 'blog-slug', params: { slug: article.slug } }"
    class="flex flex-col transition-shadow duration-150 ease-in-out shadow-sm hover:shadow-md rounded-2xl"
  >
    <div class="overflow-hidden rounded-2xl">
      <img
        v-if="article.img"
        class="h-64 w-full object-cover"
        :src="article.img"
      />
    </div>
    <!-- class="h-48 xxlmin:w-1/2 xxlmax:w-full object-cover" -->

    <div class="p-6 flex flex-col justify-between xxlmin:w-1/2 xxlmax:w-full">
      <p class="text-xs font-thin pb-8">{{ article.createdAt }}</p>
      <h2 class="text-lg font-bold pb-8">{{ article.title }}</h2>
      <p class="test-base font-light pb-8">{{ article.description }}</p>
    </div>
  </NuxtLink>
</template>

<script>
export default {
  props: {
    article: { type: Object, default: () => {} },
  },
  data() {
    return {}
  },
}
</script>
/
