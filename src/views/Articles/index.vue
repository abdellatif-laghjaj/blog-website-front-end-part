<template>
  <InnerPageHero title="Our Articles" image-url="/images/articles.jpg"/>

  <div class="mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <Articles :show-view-more="false" :articles="articles.data"/>

    <!-- Show more -->
    <div class="flex justify-center mt-4" v-if="articles.links.next !== null">
      <button class="btn gap-2 flex items-center gap-2" @click="showMoreArticles"
              v-if="!loading">
        <span>Load More</span>
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"></path>
        </svg>
      </button>
      <button class="btn loading" v-else>loading</button>
    </div>
  </div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import Articles from "@/components/Articles";
import {useArticle} from "@/composables/useArticle";

export default {
  name: "index",
  components: {Articles, InnerPageHero},
  props: {},

  setup() {
    let {fetchArticles, loading, articles} = useArticle();
    // Fetch articles
    fetchArticles();

    //show more articles
    const showMoreArticles = () => {
      fetchArticles({
        showMore: true,
        page: articles.value.meta.current_page + 1
      });
    }

    return {
      articles,
      loading,
      showMoreArticles,
    }
  },
}
</script>

<style scoped>

</style>