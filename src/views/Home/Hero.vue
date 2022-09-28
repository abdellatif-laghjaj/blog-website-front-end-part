<template>
  <div class="hero min-h-screen">
    <img :src="domain + settings.hero_image_url" alt="hero image" class="block w-full h-full object-cover">
    <div class="hero-overlay bg-opacity-80"></div>
    <div class="hero-content text-center text-white sm:mt-[-10rem]">
      <div class="max-w-md">
        <h1 class="mb-1 text-4xl font-bold">Welcome to</h1>
        <h1 class="mb-5 text-4xl font-bold">Abdel. <span class="text-primary">Blog</span></h1>
        <p class="mb-5" v-html="settings.hero_description"></p>
        <router-link to="/articles" class="btn btn-primary mx-1">Read Articles</router-link>
        <router-link to="/contact" class="btn btn-secondary mx-1">Contact us</router-link>
      </div>
    </div>
  </div>
</template>

<script>
import {useSettings} from "@/composables/useSettings";
import {ref} from "vue";

export default {
  name: "Hero",

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