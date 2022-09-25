<template>
  <div>
    <NavBar/>

    <router-view/>

    <div>
      Footer
    </div>
  </div>
</template>

<script>
import NavBar from "@/components/Layouts/NavBar";

export default {
  name: 'App',
  components: {
    NavBar
  }
};
</script>

