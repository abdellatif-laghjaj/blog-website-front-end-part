<template>
  <div>
    <div class="card lg:card-side bg-base-100 shadow-xl">
      <div class="card card-side bg-base-100 shadow-xl">
        <figure><img src="/images/hero.jpg" style="width: 200px; height: 280px; object-fit: cover;" alt="Movie"/></figure>
        <div class="card-body">
          <h2 class="card-title">New movie is released!</h2>
          <p>Click the button to watch on Jetflix app.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-primary">Watch</button>
          </div>
        </div>
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

</style>