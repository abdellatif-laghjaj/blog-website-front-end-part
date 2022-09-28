<template>
  <div class="container mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <!-- Title -->
    <h1 class="text-2xl sm:text-4xl font-bold mb-4 mt-10 text-center">{{ article.title }}</h1>
    <!-- Image -->
    <div class="mb-4 article-detail-image w-full sm:h-[400px]">
      <img :src="domain + article.image_url" alt="article image" class="w-full sm:h-full h-1/2 object-cover">
    </div>
    <!-- Category and date -->
    <div class="flex sm:items-center justify-between flex-col sm:flex-row">
      <div class="badge badge-primary flex items-center gap-1 py-3">
        <box-icon name='purchase-tag' color="#fff" size="16px"></box-icon>
        <span>{{ article.category.name }}</span>
      </div>

      <div class="flex items-center gap-1 text-gray-500 italic mt-2 sm:mt-0">
        <div>
          <box-icon name='time-five' color="#6b7280" size="18px"></box-icon>
        </div>
        <div>{{ article.created_date }}</div>
      </div>
    </div>

    <!-- Article Body -->
    <div class="mt-4 sm:mt-16">
      <div v-html="article.description"></div>
    </div>
  </div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import {useArticle} from "@/composables/useArticle";
import 'boxicons'
import {ref} from "vue";

export default {
  name: "show",
  components: {InnerPageHero},

  props: {
    slug: {
      type: String,
    }
  },

  setup(props) {
    let {articleDetail, articleDetailLoading, fetchArticleDetail} = useArticle();
    const domain = ref('http://localhost');

    //fetch article detail
    fetchArticleDetail({
      slug: props.slug
    });

    return {
      domain,
      article: articleDetail,
      loading: articleDetailLoading,
    }
  },
}
</script>