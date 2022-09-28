<template xmlns="http://www.w3.org/1999/html">
  <div class="card w-96 bg-base-100 shadow-xl mx-2">
    <figure>
      <img :src="domain + article.image_url" class="article-img" :alt="article.title">
    </figure>
    <div class="card-body">
      <h2 class="card-title text-2xl transition-colors duration-300 hover:text-primary">
        <router-link :to="`/articles/${article.slug}`">{{ article.title }}</router-link>
      </h2>
      <div class="text-gray-500 italic mb-2 flex items-center gap-1">
        <div>
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
          </svg>
        </div>
        <div>{{ article.created_at_for_human }}</div>
      </div>
      <p>{{ article.small_description }}</p>
      <div class="card-actions justify-end">
        <div class="badge badge-secondary">{{ article.category.name }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import {ref} from "vue";

export default {
  props: {
    article: Object,
  },
  setup() {
    const domain = ref('http://localhost');
    return {
      domain
    }
  },
}
</script>

<style scoped>
.article-img {
  width: 400px;
  height: 225px;
  object-fit: cover;
}
</style>