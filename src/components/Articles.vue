<template>
  <div>
    <!-- Articles -->
    <div class="flex justify-center flex-wrap gap-5 mx-auto">
      <Article/>
      <Article/>
      <Article/>
      <Article/>
      <Article/>
      <Article/>
    </div>

    <!-- Show more -->
    <div class="flex justify-center mt-4">
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
  props: {},
  setup() {
    return {}
  },
}
</script>

<style scoped>

</style>