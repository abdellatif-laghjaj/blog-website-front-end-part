<template>
  <div class="navbar bg-base-100 shadow-lg">
    <div class="navbar-start">
      <div class="dropdown">
        <label tabindex="0" class="btn btn-ghost lg:hidden">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16"/>
          </svg>
        </label>
        <ul tabindex="0" class="menu menu-compact dropdown-content mt-3 p-2 shadow bg-base-100 rounded-box w-52">
          <NavBarLink to="/articles" label="Articles"/>
          <NavBarLink to="/about" label="About"/>
          <NavBarLink to="/contact" label="Contact"/>
        </ul>
      </div>
      <router-link to="/">
        <a class="btn btn-ghost normal-case text-xl">
          Abdel. <span class="text-primary">Blog</span>
        </a>
      </router-link>
    </div>
    <div class="navbar-end hidden lg:flex">
      <ul class="menu menu-horizontal p-0">
        <NavBarLink to="/articles" label="Articles"/>
        <NavBarLink to="/about" label="About"/>
        <NavBarLink to="/contact" label="Contact"/>
      </ul>
    </div>
  </div>
</template>

<script>
import 'boxicons'
import NavBarLink from "@/components/Layouts/NavBarLink";

export default {
  props: {},
  setup() {
    return {}
  },
  components: {
    NavBarLink
  }
}
</script>

<style scoped>

</style>