<template xmlns="http://www.w3.org/1999/html">
  <div class="card w-96 bg-base-100 shadow-xl mx-2">
    <figure>
      <img src="/images/hero.jpg" class="article-img" alt="Shoes"/>
    </figure>
    <div class="card-body">
      <h2 class="card-title text-2xl transition-colors duration-300 hover:text-primary">
        <router-link to="/articles/article-slug">Article Title</router-link>
      </h2>
      <div class="text-gray-500 italic mb-2 flex items-center gap-1">
        <box-icon name='time-five' color="#6b7280" size="19px"></box-icon>
        <div>5 hours ago</div>
      </div>
      <p>If a dog chews shoes whose shoes does he choose?</p>
      <div class="card-actions justify-end">
        <div class="badge badge-secondary">Fashion</div>
        <div class="badge badge-secondary">Products</div>
      </div>
    </div>
  </div>
</template>

<script>
import 'boxicons'

export default {
  props: {},
  setup() {
    return {}
  },
}
</script>

<style scoped>
.article-img {
  width: 400px;
  height: 225px;
  object-fit: cover;
}
</style>