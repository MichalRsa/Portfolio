<template>
  <h2 class="text-3xl my-8">{{ title }}</h2>
</template>

<script lang="ts">
export default {
  props: { title: { type: String, required: true } },
}
</script>
