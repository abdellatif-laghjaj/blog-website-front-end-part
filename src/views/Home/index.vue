<template>
  <div>
    <Hero/>
    <!-- Articles -->
    <div class="py-8 sm:py-20 sm:px-0 container mx-auto">
      <Articles :articles="articles.data"/>
    </div>
  </div>
</template>

<script>
import Hero from "@/views/Home/Hero";
import Articles from "@/components/Articles";
import {useArticle} from "@/composables/useArticle";

export default {
  name: 'Home',
  components: {
    Hero,
    Articles,
  },

  setup() {
    // let {articles, loading, fetchArticles} = useArticle();
    let {fetchArticles, articles} = useArticle();
    // Fetch articles
    fetchArticles();

    return {
      articles,
    }
  }
};
</script>

<style scoped>

</style>