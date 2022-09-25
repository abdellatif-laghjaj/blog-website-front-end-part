<template>
  <div>
    <!-- Articles -->
    <div class="m-4 lg:flex lg:flex-wrap justify-center gap-6">
      <Article/>
      <Article/>
      <Article/>
      <Article/>
      <Article/>
      <Article/>
    </div>

    <!-- Show more -->
    <div>
      <router-link to="/article">
        <button class="btn gap-2">
          Load more
          <box-icon name='loader-circle' color="#fff"></box-icon>
        </button>
      </router-link>
    </div>
  </div>
</template>

<script>
import 'boxicons'
import Article from "@/components/layouts/Article";

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