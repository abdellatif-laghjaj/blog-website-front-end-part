<template>
  <InnerPageHero title="Our" subtitle="Articles" image-url="/images/articles.jpg"/>

  <div class="mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <Articles :show-view-more="false"/>

    <!-- Show more -->
    <div class="flex justify-center mt-4">
      <button class="btn gap-2 flex items-center gap-2">
        <span>Load More</span>
        <box-icon name='refresh' color="#fff"></box-icon>
      </button>
    </div>
  </div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import Articles from "@/components/Articles";
import 'boxicons'

export default {
  name: "index",
  components: {Articles, InnerPageHero}
}
</script>

<style scoped>

</style>