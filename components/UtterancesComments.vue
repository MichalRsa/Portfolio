<template>
  <div />
</template>
<script>
export default {
  mounted() {
    const scriptTag = document.createElement('script')
    scriptTag.setAttribute('src', 'https://utteranc.es/client.js')
    scriptTag.setAttribute('repo', 'MichalRsa/michalrosa.dev-comments')
    scriptTag.setAttribute('issue-term', 'pathname')
    scriptTag.setAttribute('label', 'documentation')
    scriptTag.setAttribute('theme', 'github-light')
    scriptTag.setAttribute('crossorigin', 'anonymous')
    scriptTag.setAttribute('async', 'async')
    this.$el.append(scriptTag)
  },
}
</script>
