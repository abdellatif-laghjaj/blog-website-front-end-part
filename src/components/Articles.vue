<template>
  <div>
    <!-- Articles -->
    <div class="flex justify-center flex-wrap gap-5 mx-auto">
      <Article v-for="article in articles" :key="article.id" :article="article"/>
    </div>

    <!-- Show more -->
    <div class="flex justify-center mt-4" v-if="showViewMore">
      <router-link to="/articles">
        <button class="btn gap-2 flex items-center gap-2">
          <span>View More</span>
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
          </svg>
        </button>
      </router-link>
    </div>
  </div>
</template>

<script>
import 'boxicons'
import Article from "@/components/Article";

export default {
  components: {Article},
  props: {
    showViewMore: {
      type: Boolean,
      default: true
    },
    articles: Array,
  },
  setup() {
  },
}
</script>

<style scoped>

</style>