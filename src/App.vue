<template>
  <div>
    <NavBar/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import NavBar from "@/components/layouts/NavBar";
import Footer from "@/components/layouts/Footer";

export default {
  name: 'App',
  components: {
    NavBar,
    Footer,
  }
};
</script>

