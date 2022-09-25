<template>
  <li class="mx-1">
    <router-link :to="to">{{ label }}</router-link>
  </li>
</template>

<script>
export default {
  props: {
    to: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true
    }
  },

  setup(props) {
    return {
      to: props.to,
      label: props.label
    }
  }
}
</script>

<style scoped>

</style>