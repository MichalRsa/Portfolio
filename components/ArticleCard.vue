<template>
  <NuxtLink
    :to="{ name: 'blog-slug', params: { slug: article.slug } }"
    class="flex flex-col transition-shadow duration-150 ease-in-out shadow-sm hover:shadow-md rounded-2xl"
  >
    <div class="sm:h-64 h-44">
      <div class="w-full h-full overflow-hidden rounded-2xl">
        <img
          v-if="article.img"
          class="min-w-full min-h-full object-cover"
          :src="article.img"
        />
      </div>
    </div>

    <div
      class="p-4 flex flex-col justify-start xxlmin:w-1/2 xxlmax:w-full md:h-64 h-auto"
    >
      <p class="text-xs font-thin pb-4">{{ article.createdAt }}</p>
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
