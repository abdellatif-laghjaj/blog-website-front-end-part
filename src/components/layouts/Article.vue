<template>
  <div class="card w-96 bg-base-100 shadow-xl mx-2">
    <figure>
      <img src="/images/hero.jpg" class="article-img" alt="Shoes"/>
    </figure>
    <div class="card-body">
      <h2 class="card-title text-2xl">
        Shoes!
      </h2>
      <p class="opacity-80 italic mb-2">5 hours ago</p>
      <p>If a dog chews shoes whose shoes does he choose?</p>
      <div class="card-actions justify-end">
        <div class="badge badge-secondary">Fashion</div>
        <div class="badge badge-secondary">Products</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {},
  setup() {
    return {}
  },
}
</script>

<style scoped>
.article-img{
  width: 400px;
  height: 225px;
  object-fit: cover;
}
</style>