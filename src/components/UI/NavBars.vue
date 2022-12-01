<template>
  <ul>
    <nav-bar v-for="page in pages" :page="page" :key="page.name" />
  </ul>
</template>
<script>
import NavBar from "./NavBar.vue";
export default {
  components: { NavBar },
  name: "NavBars",
  props: {
    pages: Array,
  },
};
</script>
<style scoped>
ul {
  list-style: none;
  padding: 0;
}
</style>