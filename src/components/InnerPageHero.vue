<template>
  <div class="relative z-0 h40 sm:h-64">
    <img :src="imageUrl" alt="about image" class="h-full w-full object-cover">

    <div class="absolute inset-0 bg-black opacity-50"></div>
    <div class="absolute inset-0 bg-gradient-to-t from-primary opacity-50"></div>

    <div class="absolute inset-0">
      <div
          class="container mx-auto px-4 sm:px-0 text-white text-3xl sm:text-4xl mt-[2rem] font-bold h-full w-full flex items-center justify-center gap-1">
        <span>{{ title }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "InnerPageHero",
  props: {
    title: {
      type: String,
      required: true
    },
    imageUrl: {
      type: String,
      required: true
    }
  },

  setup(props) {
    return {
      title: props.title,
      imageUrl: props.imageUrl
    }
  }
}
</script>

<style scoped>

</style>