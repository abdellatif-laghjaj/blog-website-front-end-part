<template>
  <InnerPageHero title="Our" subtitle="Articles" image-url="/images/articles.jpg"/>

  <div class="mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <Articles :shwo-view-more="false"/>
  </div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import Articles from "@/components/Articles";

export default {
  name: "index",
  components: {Articles, InnerPageHero}
}
</script>

<style scoped>

</style>