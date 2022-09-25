<template>
  <InnerPageHero title="Contact" subtitle="Us" image-url="/images/contact.jpg"/>

  <div class="container mx-auto py-8 px-4 sm:py-12 sm:px-8">
    <div class="grid sm:grid-cols-3 sm:gap-4">
      <div><span class="font-bold">Adress:</span> <span
          class="text-gray-500">1234 Street Name, City Name, United States</span></div>
      <div><span class="font-bold">Phone:</span> <span class="text-gray-500">(123) 456-7890</span></div>
      <div><span class="font-bold">Email:</span> <span class="text-gray-500">example@gmail.com</span></div>
    </div>

    <div class="mt-8 sm:mt-16 grid sm:grid-cols-2 gap-8 sm-gap-12">
      <div>
        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d387195.65931207524!2d-74.52106375377763!3d40.69674450347907!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24fa5d33f083b%3A0xc80b8f06e177fe62!2sNew%20York%2C%20NY%2C%20USA!5e0!3m2!1sen!2sma!4v1664136080960!5m2!1sen!2sma"
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

export default {
  name: "index",
  components: {InnerPageHero}
}
</script>

<style scoped>

</style>