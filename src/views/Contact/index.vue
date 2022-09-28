<template>
  <InnerPageHero title="Contact Us" :image-url="domain + settings.contact_image_url"/>

  <div class="container mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <div class="grid sm:grid-cols-3 sm:gap-4">
      <div><span class="font-bold">Adress:</span> <span
          class="text-gray-500">{{ settings.address }}</span></div>
      <div><span class="font-bold">Phone:</span> <span class="text-gray-500">{{ settings.phone }}</span></div>
      <div><span class="font-bold">Email:</span> <span class="text-gray-500">{{ settings.email }}</span></div>
    </div>

    <div class="mt-8 sm:mt-16 grid sm:grid-cols-2 gap-8 sm-gap-12">
      <div>
        <iframe
            :src="settings.google_map_url"
            class="w-full h-full" style="border:0;" allowfullscreen="" loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>

      <!-- Contact Form -->
      <form class="card flex-shrink-0 w-full shadow-2xl bg-base-100">
        <div class="card-body w-full">
          <h2 class="text-center font-bold text-2xl mb-2">Contact <span class="text-primary">Form</span></h2>
          <div class="form-control">
            <input type="text" placeholder="Full name" class="input input-bordered" required/>
            <!--            <span class="text-error text-sm py-3">Name is required</span>-->
          </div>
          <div class="form-control">
            <input type="text" placeholder="Message subject" class="input input-bordered" required/>
            <!--            <span class="text-error text-sm py-3">Subject is required</span>-->
          </div>
          <div class="form-control">
            <input type="email" placeholder="Email" class="input input-bordered" required/>
            <!--            <span class="text-error text-sm py-3">Email is required</span>-->
          </div>
          <div class="form-control">
            <input type="tel" placeholder="Phone number" class="input input-bordered" required/>
            <!--            <span class="text-error text-sm py-3">Phone is required</span>-->
          </div>
          <div class="form-control">
            <textarea class="textarea textarea-bordered" placeholder="Type your message here..." required></textarea>
            <!--            <span class="text-error text-sm py-3">Message is required</span>-->
          </div>

          <!-- Success message -->
          <!--          <div class="alert alert-success shadow-lg none">-->
          <!--            <div>-->
          <!--              <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current flex-shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>-->
          <!--              <span>Your message has been sent successfully.</span>-->
          <!--            </div>-->
          <!--          </div>-->

          <!-- Error message -->
          <!--          <div class="alert alert-error shadow-lg">-->
          <!--            <div>-->
          <!--              <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current flex-shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>-->
          <!--              <span>Something went wrong. Please try again later.</span>-->
          <!--            </div>-->
          <!--          </div>-->

          <div class="form-control mt-3">
            <button class="btn btn-primary">send message</button>
          </div>
        </div>
      </form>
    </div>
  </div>
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