<template>
  <div class="container">
    <AboutMe />
    <div class="content">
      <main>
        <ArticleCard
          v-for="article in articles"
          :key="article.slug"
          v-bind="article"
        />
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      articles: [
        {
          title: 'mi-primer-post',
          slug: 'mi-primer-post',
          date: new Date(),
        },
      ],
    }
  },
}
</script>

<style lang="scss">
.container {
  @apply m-auto;
}
.container .content {
  @apply flex flex-col justify-center items-center sm:p-2 md:p-4 lg:p-8 xl:p-16;
  main {
    @apply max-w-5xl grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6;
  }
}
</style>
