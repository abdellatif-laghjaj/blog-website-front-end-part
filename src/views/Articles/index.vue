<template>
  <InnerPageHero title="Our" subtitle="Articles" image-url="/images/articles.jpg"/>

  <div class="mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <Articles :show-view-more="false" :articles="articles.data"/>

    <!-- Show more -->
    <div class="flex justify-center mt-4" v-if="articles.links.next !== null">
      <button class="btn gap-2 flex items-center gap-2" @click="showMoreArticles"
              v-if="!loading">
        <span>Load More</span>
        <box-icon name='refresh' color="#fff"></box-icon>
      </button>
      <button class="btn loading" v-else>loading</button>
    </div>
  </div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import Articles from "@/components/Articles";
import {useArticle} from "@/composables/useArticle";
import 'boxicons'

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