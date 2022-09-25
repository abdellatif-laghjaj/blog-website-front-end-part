<template>
  <InnerPageHero title="Article" subtitle="Details" image-url="/images/article-details.jpg"/>

  <div class="container mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <!-- Category and date -->
    <div class="flex sm:items-center justify-between flex-col sm:flex-row">
      <div class="badge badge-primary flex items-center gap-1 py-3">
        <box-icon name='purchase-tag' color="#fff" size="16px"></box-icon>
        <span>Technology</span>
      </div>

      <div class="flex items-center gap-1 text-gray-500 italic mt-2 sm:mt-0">
        <div>
          <box-icon name='time-five' color="#6b7280" size="18px"></box-icon>
        </div>
        <div>12 May 2021</div>
      </div>
    </div>

    <!-- Article Body -->
    <div class="mt-4 sm:mt-16">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam ipsa labore repellat sit. Ab accusantium
        adipisci corporis eligendi et ex exercitationem itaque labore magnam minima quos, unde veritatis? Beatae itaque
        magnam nostrum perferendis porro totam voluptas? A ad, alias aliquam asperiores beatae, distinctio eos error,
        est ex iure nobis omnis.
      </p>
      <p class="mt-4">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam ipsa labore repellat sit. Ab accusantium
        adipisci corporis eligendi et ex exercitationem itaque labore magnam minima quos, unde veritatis? Beatae itaque
        magnam nostrum perferendis porro totam voluptas? A ad, alias aliquam asperiores beatae, distinctio eos error,
        est ex iure nobis omnis.
      </p>
      <p class="mt-4">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam ipsa labore repellat sit. Ab accusantium
        adipisci corporis eligendi et ex exercitationem itaque labore magnam minima quos, unde veritatis? Beatae itaque
        magnam nostrum perferendis porro totam voluptas? A ad, alias aliquam asperiores beatae, distinctio eos error,
        est ex iure nobis omnis.
      </p>
      <p class="mt-4">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam ipsa labore repellat sit. Ab accusantium
        adipisci corporis eligendi et ex exercitationem itaque labore magnam minima quos, unde veritatis? Beatae itaque
        magnam nostrum perferendis porro totam voluptas? A ad, alias aliquam asperiores beatae, distinctio eos error,
        est ex iure nobis omnis.
      </p>
    </div>
  </div>
</template>

<script>
import InnerPageHero from "@/components/InnerPageHero";
import 'boxicons'

export default {
  name: "show",
  components: {InnerPageHero}
}
</script>

<style scoped>

</style>