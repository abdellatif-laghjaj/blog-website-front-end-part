<template>
  <div class="hero min-h-screen">
    <img src="/images/hero.jpg" alt="hero image" class="block w-full h-full object-cover">
    <div class="hero-overlay bg-opacity-80"></div>
    <div class="hero-content text-center text-white sm:mt-[-10rem]">
      <div class="max-w-md">
        <h1 class="mb-1 text-4xl font-bold">Welcome to</h1>
        <h1 class="mb-5 text-4xl font-bold">Abdel. <span class="text-primary">Blog</span></h1>
        <p class="mb-5">A modern blog website talk about technology, programming, and more.</p>
        <p class="mb-5">This blog is built with Laravel and Vue.js.</p>
        <router-link to="/articles" class="btn btn-primary mx-1">Read Articles</router-link>
        <router-link to="/contact" class="btn btn-secondary mx-1">Contact us</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero"
}
</script>

<style scoped>

</style>