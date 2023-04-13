<template>
  <main>
    <ContentDoc />
  </main>
  <article>
    <nuxt-content :document="article" />
    article xd
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('/', params.slug).fetch()
    console.log(article);
    return { article }
  }
}
</script>
