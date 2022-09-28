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
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M7 7h.01M7 3h5c.512 0 1.024.195 1.414.586l7 7a2 2 0 010 2.828l-7 7a2 2 0 01-2.828 0l-7-7A1.994 1.994 0 013 12V7a4 4 0 014-4z"></path>
        </svg>
        <span>{{ article.category.name }}</span>
      </div>

      <div class="flex items-center gap-1 text-gray-500 italic mt-2 sm:mt-0">
        <div>
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
          </svg>
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