<template>
  <div>
    <Hero/>
    <!-- Articles -->
    <div class="py-8 sm:py-20 sm:px-0 container mx-auto">
      <Articles/>
    </div>
  </div>
</template>

<script>
import Hero from "@/views/Home/Hero";
import Articles from "@/components/Articles";

export default {
  name: 'Home',
  components: {
    Hero,
    Articles,
  }
};
</script>

<style scoped>

</style>