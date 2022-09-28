<template>
  <InnerPageHero title="About Us" :image-url="domain + settings.about_image_url"/>

  <div class="container mx-auto py-8 px-4 sm:py-12 sm:px-8" v-html="settings.about_description"></div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import {useSettings} from "@/composables/useSettings";
import {ref} from "vue";

export default {
  name: "index",
  components: {InnerPageHero},
  setup() {
    let {settings} = useSettings();
    const domain = ref('http://127.0.0.1:8000');

    return {
      settings,
      domain,
    }
  }
}
</script>

<style scoped>

</style>