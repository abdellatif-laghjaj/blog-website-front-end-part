<template>
  <div class="flex flex-col h-full ">
    <NavBar/>
    <div class="flex-1">
      <router-view/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import NavBar from "@/components/layouts/NavBar";
import Footer from "@/components/layouts/Footer";
import {useSettings} from "@/composables/useSettings";

export default {
  name: 'App',
  components: {
    NavBar,
    Footer,
  },

  setup() {
    let {fetchSettings} = useSettings();
    fetchSettings();
  }
};
</script>

