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
          <box-icon name='link-external' color="#fff"></box-icon>
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